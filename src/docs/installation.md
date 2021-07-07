# Node.js versions

Compodoc is tested with only LTS versions : v12.x, v14.x

# Angular-CLI

Compodoc supports last Angular-CLI version : 12.x

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

Create a file named `tsconfig.doc.json`, containing a key `include` pointing to `src` folder, you can also use `exclude` key :

```
{
  "include": ["src/**/*.ts"],
  "exclude": ["src/test.ts", "src/**/*.spec.ts", "src/app/file-to-exclude.ts"]
}
```

Define a script task for it in your package.json (with npm 6.x) :

```bash
"scripts": {
  "compodoc": "npx compodoc -p tsconfig.doc.json"
}
```

and run it like a normal npm script :

```bash
npm run compodoc
```

or with npx :

```bash
npx @compodoc/compodoc ...
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
│ └── ...
├── tsconfig.app.json
├── tsconfig.doc.json
└── tsconfig.json
```
