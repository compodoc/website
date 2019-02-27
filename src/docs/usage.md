```bash
compodoc <src> [options]
```

# Options :

| Flag                                      | Description                                                                                                                                                                                                                                                                                                 |
| ----------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **-h, --help**                            | output usage information                                                                                                                                                                                                                                                                                    |
| **-V, --version**                         | output the version number                                                                                                                                                                                                                                                                                   |
| **-c, --config [config]**                 | A configuration file : .compodocrc, .compodocrc.json, .compodocrc.yaml or compodoc property in package.json                                                                                                                                                                                                 |
| **-p, --tsconfig [config]**               | A tsconfig.json file                                                                                                                                                                                                                                                                                        |
| **-d, --output [folder]**                 | Where to store the generated documentation                                                                                                                                                                                                                                                                  |
| **-y, --extTheme [file]**                 | External styling theme                                                                                                                                                                                                                                                                                      |
| **-n, --name [name]**                     | Title of the documentation                                                                                                                                                                                                                                                                                  |
| **-a, --assetsFolder [folder]**           | External assets folder to copy in generated documentation folder                                                                                                                                                                                                                                            |
| **-o, --open**                            | Open the generated documentation                                                                                                                                                                                                                                                                            |
| **-t, --silent**                          | In silent mode, log messages aren't logged in the console                                                                                                                                                                                                                                                   |
| **-s, --serve**                           | Serve generated documentation (default http://localhost:8080/)                                                                                                                                                                                                                                              |
| **-r, --port [port]**                     | Change default serving port                                                                                                                                                                                                                                                                                 |
| **-w, --watch**                           | Watch source files after serve and force documentation rebuild                                                                                                                                                                                                                                              |
| **-e, --exportFormat [format]**           | Export in specified format (json, html (default))                                                                                                                                                                                                                                                           |
| **--language [language]**                 | Language used for the generated documentation (en-US, fr-FR, zh-CN, pt-BR) (default: en-US)                                                                                                                                                                                                                 |
| **--theme [theme]**                       | Choose one of available themes, default is 'gitbook' (laravel, original, material, postmark, readthedocs, stripe, vagrant)                                                                                                                                                                                  |
| **--hideGenerator**                       | Do not print the Compodoc logo at the bottom of the page                                                                                                                                                                                                                                                    |
| **--toggleMenuItems <items>**             | Close by default items in the menu (default ['all']) values : ['all'] or one of these ['modules','components','directives','classes','injectables','interfaces','pipes','additionalPages'])                                                                                                                 |
| **--navTabConfig <tab configs>**          | List navigation tab objects in the desired order with two string properties ("id" and "label"). Double-quotes must be escaped with '\\'. Available tab IDs are "info", "readme", "source", "templateData", "tree", and "example". Note: Certain tabs will only be shown if applicable to a given dependency |
| **--templates [folder]**                  | Path to directory of Handlebars templates to override built-in templates                                                                                                                                                                                                                                    |
| **--includes [path]**                     | Path of external markdown files to include                                                                                                                                                                                                                                                                  |
| **--includesName [name]**                 | Name of item menu of externals markdown files (default "Additional documentation")                                                                                                                                                                                                                          |
| **--coverageTest**                        | Test command of documentation coverage with a threshold (default 70)                                                                                                                                                                                                                                        |
| **--coverageMinimumPerFile [minimum]**    | Test command of documentation coverage per file with a minimum (default 0)                                                                                                                                                                                                                                  |
| **--coverageTestThresholdFail [boolean]** | Test command of documentation coverage (global or per file) will fail with error or just warn user (true: error, false: warn) (default: true)                                                                                                                                                               |
| **--coverageTestShowOnlyFailed**          | Display only failed files for a coverage test                                                                                                                                                                                                                                                               |
| **--unitTestCoverage [json-summary]**     | To include unit test coverage, specify istanbul JSON coverage summary file                                                                                                                                                                                                                                  |
| **--disableSourceCode**                   | Do not add source code tab and links to source code                                                                                                                                                                                                                                                         |
| **--disableDomTree**                      | Do not add dom tree tab                                                                                                                                                                                                                                                                                     |
| **--disableTemplateTab**                  | Do not add template tab                                                                                                                                                                                                                                                                                     |
| **--disableStyleTab**                     | Do not add style tab                                                                                                                                                                                                                                                                                        |
| **--disableGraph**                        | Disable rendering of the dependency graph                                                                                                                                                                                                                                                                   |
| **--disableCoverage**                     | Do not add the documentation coverage report                                                                                                                                                                                                                                                                |
| **--disablePrivate**                      | Do not show private in generated documentation                                                                                                                                                                                                                                                              |
| **--disableProtected**                    | Do not show protected in generated documentation                                                                                                                                                                                                                                                            |
| **--disableInternal**                     | Do not show @internal in generated documentation                                                                                                                                                                                                                                                            |
| **--disableLifeCycleHooks**               | Do not show Angular lifecycle hooks in generated documentation                                                                                                                                                                                                                                              |
| **--disableRoutesGraph**                  | Do not add the routes graph                                                                                                                                                                                                                                                                                 |
| **--disableSearch**                       | Do not add the search input                                                                                                                                                                                                                                                                                 |
| **--minimal**                             | Minimal mode with only documentation. No search, no graph, no coverage.                                                                                                                                                                                                                                     |
| **--customFavicon [path]**                | Use a custom favicon                                                                                                                                                                                                                                                                                        |
| **--customLogo [path]**                   | Use a custom logo                                                                                                                                                                                                                                                                                           |
| **--gaID [id]**                           | Google Analytics tracking ID                                                                                                                                                                                                                                                                                |
| **--gaSite [site]**                       | Google Analytics site name (default auto (default: auto)                                                                                                                                                                                                                                                    |

# Configuration file

You can provide a configuration file in the root of your project folder.

Compodoc will search files like : .compodocrc, .compodocrc.json, .compodocrc.yaml or a compodoc property in your package.json

A JSON schema is available here : `./node_modules/@compodoc/compodoc/src/config/schema.json`

# Options, quotes and Windows usage

Keep in mind that using options with multiple words need quotes around your sentence.

```bash
compodoc -p src/tsconfig.json -n 'My app documentation'
```

Using npm scripts, the command is hosted in package.json file. Don't forget to escape with double quotes for Windows systems. (with npm 6.x)

```bash
{
   ...
   "doc": "npx compodoc -p src/tsconfig.app.json -n \"My app documentation\""
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
