# Hosting

Once you have the documentation generated inside an output folder, you can host your documentation where you want.

## Github pages

Follow this great tutorial : https://voorhoede.github.io/front-end-tooling-recipes/travis-deploy-to-gh-pages/

## Static hosts without a Git setup

The output folder is plain HTML, CSS and JavaScript, so any static host works. If you just need a shareable link without setting up a repository or CI, you can upload the folder in one request to [deed.page](https://deed.page) (replace `my-app-docs` with your own slug) :

```bash
compodoc -p tsconfig.doc.json
tar -C documentation -czf documentation.tar.gz .
curl -T documentation.tar.gz "https://deed.page/v1/sites?slug=my-app-docs"
```

The JSON response contains the URL (`https://my-app-docs.deed.page/`) and a token. Keep the token and send it as `Authorization: Bearer <token>` with the same command to update the documentation after the next build. See the [deed.page docs](https://deed.page/docs) for limits.
