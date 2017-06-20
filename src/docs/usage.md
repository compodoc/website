```bash
compodoc <src> [options]
```

# Options :
|            |           |
|------------|-----------|
| __ -h, --help __ | output usage information |
| __ -V, --version __ | output the version number |
| __ -p, --tsconfig [config] __ | A tsconfig.json file |
| __ -d, --output [folder] __ | Where to store the generated documentation |
| __ -y, --extTheme [file] __ | External styling theme |
| __ -n, --name [name] __ | Title of the documentation |
| __ -a, --assetsFolder [folder] __ | External assets folder to copy in generated documentation folder |
| __ -o, --open __ | Open the generated documentation |
| __ -t, --silent __ | In silent mode, log messages aren't logged in the console |
| __ -s, --serve __ | Serve generated documentation (default http://localhost:8080/) |
| __ -r, --port [port] __ | Change default serving port |
| __ -w, --watch __ | Watch source files after serve and force documentation rebuild |
| __ --theme [theme] __ | Choose one of available themes, default is 'gitbook' (laravel, original, postmark, readthedocs, stripe, vagrant) |
| __ --hideGenerator __ | Do not print the Compodoc logo at the bottom of the page |
| __ --toggleMenuItems <items> __ | Close by default items in the menu ( example: 'all' or 'modules','components' ) |
| __ --includes [path] __ | Path of external markdown files to include
| __ --includesName [name] __ | Name of item menu of externals markdown files (default "Additional documentation")
| __ --coverageTest __ | Test command of documentation coverage with a threshold (default 70)
| __ --disableSourceCode __ | Do not add source code tab and links to source code
| __ --disableGraph __ | Disable rendering of the dependency graph
| __ --disableCoverage __ | Do not add the documentation coverage report
| __ --disablePrivateOrInternalSupport __ | Do not show private, @internal or Angular lifecycle hooks in generated documentation

# Options, quotes and Windows usage

Keep in mind that using options with multiple words need quotes around your sentence.

```bash
compodoc -p src/tsconfig.json -n 'My app documentation'
```

Using npm scripts, the command is hosted in package.json file. Don't forget to escape with double quotes for Windows systems.

```bash
{
   ...
   "doc": "./node_modules/.bin/compodoc -p src/tsconfig.app.json -n \"My app documentation\""
   ...
}
```

# Render documentation

Documentation is generated in default output folder, then run your HTTP server in that folder.

```bash
compodoc -p src/tsconfig.json
```

# Render documentation while providing source folder

```bash
compodoc src -p src/tsconfig.json
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
compodoc -p src/tsconfig.json -s
```
