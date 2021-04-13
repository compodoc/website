# Configuration file

You can provide a configuration file in the root of your project folder.

Compodoc will search files like : .compodocrc, .compodocrc.json, .compodocrc.yaml or a compodoc property in your package.json

A JSON schema is available here : `./node_modules/@compodoc/compodoc/src/config/schema.json`

# Options, quotes and Windows usage

Keep in mind that using options with multiple words need quotes around your sentence.

```bash
compodoc -p tsconfig.doc.json -n 'My app documentation'
```

Using npm scripts, the command is hosted in package.json file. Don't forget to escape with double quotes for Windows systems. (with npm 6.x)

```bash
{
   ...
   "doc": "npx compodoc -p tsconfig.doc.json -n \"My app documentation\""
   ...
}
```

# Render documentation

Documentation is generated in default output folder, then run your HTTP server in that folder.

```bash
compodoc -p tsconfig.doc.json
```

# Render documentation while providing source folder

```bash
compodoc src -p tsconfig.doc.json
```

# Serve generated documentation with compodoc

Documentation was generated in default output folder or a specific one, the local HTTP server is launched at http://localhost:8080

```bash
compodoc -s

or

compodoc -s -d ./doc
```

# Render documentation, and serve it with compodoc

Documentation is generated in default output folder, and a local HTTP server is available at http://localhost:8080

```bash
compodoc -p tsconfig.doc.json -s
```
