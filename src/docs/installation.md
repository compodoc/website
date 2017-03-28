### Global installation

Install from npm :

```bash
npm install -g compodoc
```

### Local installation

```bash
npm install --save-dev compodoc
```

Define a script task for it in your package.json :

```bash
"scripts": {
  "compodoc": "./node_modules/.bin/compodoc -p src/tsconfig.json"
}
```

and run it like a normal npm script :

```bash
npm run compodoc
```

See [usage](./usage.html) for details.
