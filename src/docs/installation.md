# Node.js versions

Compodoc is tested with only LTS versions : v8.11.1, v6.14.1 & v4.9.1

# Angular-CLI

Compodoc supports last Angular-CLI version : 7.x

Just run Compodoc in a fresh or existing project.

# Global installation

Install from npm :

```bash
npm install -g @compodoc/compodoc
```

If you use PowerShell on Windows, add quotes :

```bash
npm install -g "@compodoc/compodoc"
```

# Local installation

```bash
npm install --save-dev @compodoc/compodoc
```

# Run

Define a script task for it in your package.json (with npm 6.x) :

```bash
"scripts": {
  "compodoc": "npx compodoc -p src/tsconfig.app.json"
}
```

and run it like a normal npm script :

```bash
npm run compodoc
```

See [usage](./usage.html) for more details.

# Position of tsconfig file in codebase

Compodoc start at the folder level of the tsconfig file provided with `-p` option.

Example for an Angular CLI project :

```
.
├── src
│ ├── app
│ │ ├── app.component.ts
│ │ └── app.module.ts
│ ├── main.ts
│ ├── ...
│ └── tsconfig.app.json
└── tsconfig.json
```

```bash
compodoc -p src/tsconfig.app.json
```
