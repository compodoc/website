```bash
$ compodoc --help

Usage: compodoc <src> [options]

Options:

  -h, --help                         output usage information
  -V, --version                      output the version number
  -p, --tsconfig [config]            A tsconfig.json file
  -d, --output [folder]              Where to store the generated documentation
  -y, --extTheme [file]              External styling theme
  -n, --name [name]                  Title documentation
  -a, --assetsFolder [folder]        External assets folder to copy in generated documentation folder
  -o, --open                         Open the generated documentation
  -t, --silent                       In silent mode, log messages aren't logged in the console
  -s, --serve                        Serve generated documentation (default http://localhost:8080/)
  -r, --port [port]                  Change default serving port
  -w, --watch                        Watch source files after serve and force documentation rebuild
  --theme [theme]                    Choose one of available themes, default is 'gitbook' (laravel, original, postmark, readthedocs, stripe, vagrant)
  --hideGenerator                    Do not print the Compodoc link at the bottom of the page
  --toggleMenuItems <items>          Close by default items in the menu ( example: 'all' or 'modules','components' )
  --includes [path]                  Path of external markdown files to include
  --includesName [name]              Name of item menu of externals markdown files (default "Additional documentation")
  --disableSourceCode                Do not add source code tab
  --disableGraph                     Disable rendering of the dependency graph
  --disableCoverage                  Do not add the documentation coverage report
  --disablePrivateOrInternalSupport  Do not show private or @internal in generated documentation
```
