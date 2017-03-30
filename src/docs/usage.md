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
| __ --disableSourceCode __ | Do not add source code tab
| __ --disableGraph __ | Disable rendering of the dependency graph
| __ --disableCoverage __ | Do not add the documentation coverage report
| __ --disablePrivateOrInternalSupport __ | Do not show private or @internal in generated documentation
