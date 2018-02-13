# Styling the documentation
```
compodoc -p src/tsconfig.json -y your_theme_styles/
```

Inside your folder you need to provide at least a style.css file with these 5 imports as below.

```
@import "./reset.css";
@import "./bootstrap.min.css";
@import "./bootstrap-card.css";
@import "./font-awesome.min.css";
@import "./compodoc.css";
@import "./prism.css";
@import "./tablesort.css";
```

Compodoc use [bootstrap](http://getbootstrap.com/) 3.3.7. You can customize Compodoc easily.

[bootswatch.com](http://bootswatch.com/) can be a good starting point. If you want to override the default theme, just provide a bootstrap.min.css file, and it will override the default one.

```
└── your_theme_styles/
    ├── style.css // the main css file with default imports
    └── bootstrap.min.css // your bootstrap theme
```

# Documentation of each component, module, directives etc

A comment description in __xxx.component.ts__ file, between JSDoc comments can be a little short.

Compodoc search for a default __xxx.component.md__ file inside the root folder of each component, and add it inside a tab in the component page. It is the same for class, module etc.

```
└── my-component/
    ├── my.component.ts
    ├── my.component.spec.ts
    ├── my.component.scss|css
    ├── my.component.html
    └── my.component.md
```

# Additional documentation

Compodoc support the addition of external markdown files for extending the code comments of your application and the main README file.

Create a folder containing markdown files and use ```--includes``` flag to extend the documentation.
Your folder should contain a __summary.json__ file explaining the structure and files :

```
summary.json

[
    {
        "title": "A TITLE",
        "file": "a-file.md"
    },
    {
        "title": "A TITLE",
        "file": "a-file.md",
        "children": [
            {
                "title": "A TITLE",
                "file": "a-sub-folder/a-file.md"
            }
        ]
    }
]
```

Links are supported like regular markdown links.

# Syntax highlighting in markdown files

Compodoc use [Marked](https://github.com/chjj/marked) for markdown parsing and compiling to html. [prismjs.js](http://prismjs.com/) has been added for supporting syntax highlighting.

Just use a normal code block in your markdown with correct language : [Github help](https://help.github.com/articles/creating-and-highlighting-code-blocks/)

The integrated languages are : __json, bash, javascript, markdown, html, scss, typescript__

# Excluding files

For excluding files from the documentation, simply use the __exclude__ property of [__tsconfig.json__](https://www.typescriptlang.org/docs/handbook/tsconfig-json.html) file.

You can exclude specific file with name ```app/myfile.ts``` or with glob pattern ```**/*.spec.ts```.

# Including files

For including files from the documentation, simply use the __include__ property of [__tsconfig.json__](https://www.typescriptlang.org/docs/handbook/tsconfig-json.html) file.

You can include specific file with name ```app/myfile.ts``` or with glob pattern ```**/*.ts```.
