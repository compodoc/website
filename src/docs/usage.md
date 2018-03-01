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
| __ -e, --exportFormat [format] __ | Export in specified format (json, html (default)) |
| __ --theme [theme] __ | Choose one of available themes, default is 'gitbook' (laravel, original, material, postmark, readthedocs, stripe, vagrant) |
| __ --hideGenerator __ | Do not print the Compodoc logo at the bottom of the page |
| __ --toggleMenuItems <items> __ | Close by default items in the menu (default ['all']) values : ['all'] or one of these ['modules','components','directives','classes','injectables','interfaces','pipes','additionalPages']) |
| __ --includes [path] __ | Path of external markdown files to include
| __ --includesName [name] __ | Name of item menu of externals markdown files (default "Additional documentation")
| __ --coverageTest __ | Test command of documentation coverage with a threshold (default 70)
| __ --coverageMinimumPerFile [minimum] __ | Test command of documentation coverage per file with a minimum (default 0)
| __ --coverageTestThresholdFail [boolean] __ | Test command of documentation coverage (global or per file) will fail with error or just warn user (true: error, false: warn) (default: true)
| __ --disableSourceCode __ | Do not add source code tab and links to source code
| __ --disableGraph __ | Disable rendering of the dependency graph
| __ --disableCoverage __ | Do not add the documentation coverage report
| __ --disablePrivate __ | Do not show private in generated documentation
| __ --disableProtected __ | Do not show protected in generated documentation
| __ --disableInternal __ | Do not show @internal in generated documentation
| __ --disableLifeCycleHooks __ | Do not show Angular lifecycle hooks in generated documentation
| __ --disableRoutesGraph __ | Do not add the routes graph
| __ --customFavicon [path] __ | Use a custom favicon
| __ --gaID [id] __ | Google Analytics tracking ID
| __ --gaSite [site] __ | Google Analytics site name (default auto (default: auto)

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
