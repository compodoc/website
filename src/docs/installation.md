# Node.js versions

Compodoc is tested with only LTS versions : v6.9.4 & v4.7.1

# Angular-CLI

Compodoc supports last Angular-CLI version : 1.0.0

Just run Compodoc in a fresh or existing project.

# Global installation

Install from npm :

```bash
npm install -g @compodoc/compodoc
```

# Local installation

```bash
npm install --save-dev @compodoc/compodoc
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

See [usage](./usage.html) for more details.
