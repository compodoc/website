This is a simple tutorial explaining how you can document your Angular application easily with Compodoc.

We will start with a blank Angular CLI project.

# Requirements

- Angular CLI
- Node.js
- code editor or IDE

# Run Angular CLI

```bash
ng new compodoc-tutorial
```

# Install compodoc

```bash
npm i --save-dev @compodoc/compodoc
```

Add an npm script inside `package.json` file for generating the documentation, and another one for serving it :

```json
...

    "ng": "ng",
    "doc:build": "compodoc -p src/tsconfig.app.json",
    "doc:serve": "compodoc -s",
    "start": "ng serve",

...
```