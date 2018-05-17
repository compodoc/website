# Customizing tab ordering and labels

The ordering of tabs as well as the strings used for their labels can be modified by setting the `navTabConfig`
configuration item either through the compodoc config file or the CLI.

`navTabConfig` is an array of tab data. The order in which the tab data is listed is the order
in which the tabs will appear in the compodoc output. And, the string value of the label property
will appear as the label on the tab itself.

A tab is defined like this:

```
{
  "id": "info",
  "label": "Custom Label"
}
```

The tab id is used to determine which tab to apply the custom placement and label to. The available tab id's are:
__"info"__, __"readme"__, __"source"__, __"templateData"__, __"tree"__, and __"example"__.

Certain tabs will only be shown if applicable to a given dependency :

- __"info"__, __"readme"__, and __"source"__ tabs are applicable to all dependency types. 

- __"templateData"__ and __"tree"__ are applicable to Components. 

- __"example"__ tab is applicable to Component, Directive, Injectable, and Pipe dependencies.

Additionally, for certain types of tabs, if a dependency doesn't specify content for them they will not be shown even
if they are specified in the config. For example, dependencies for which no examples are provided will 
not have an "example" tab. And, the same behavior applies to the "templateData" and "readme" tabs.

### Example usage in the config file

The following example shows a list that represents the superset of tabs 
that will be shown for the various dependencies in your project.

```
{
    "navTabConfig": [
        {
            "id": "example",
            "label": "Overview"
        },
        {
            "id": "info",
            "label": "API"
        },
        {
            "id": "source",
            "label": "Source"
        },
        {
            "id": "tree",
            "label": "DOM Tree"
        }
    ],
    "tsconfig": "./src/tsconfig.json"
}
```

### Example usage as a CLI argument

Here is a similar example of `navTabConfig` usage as a CLI argument.

Note: Double-quotes must be escaped with "\\".

```
 compodoc --navTabConfig '[{\"id\": \"example\",\"label\": \"Overview\"},{\"id\": \"info\",\"label\": \"API\"},{\"id\": \"source\",\"label\": \"Source\"}]' -p src/tsconfig.json -n 'Documentation Name' -s
```