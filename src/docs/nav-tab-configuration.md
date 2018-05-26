# Customizing tab order and labels

The ordering of tabs and the text used for their labels can be modified by setting the `navTabConfig`
configuration item either through a compodoc config file or the CLI.

`navTabConfig` is an array of tab configuration objects representing the superset of tabs that will 
be shown for the various dependencies in your project. The ordering of the array determines the left-to-right 
placement of tabs in the compodoc output, and the string value of each tab configuration object's `label` 
property determines the label displayed on the corresponding tab.

## Defining a tab

```
{
  "id": "info",
  "label": "Custom Label"
}
```

The tab id is used to determine which tab to apply the custom placement and label to. The available tab id's are:
__"info"__, __"readme"__, __"source"__, __"templateData"__, __"tree"__, and __"example"__.

## Additional information

Certain tabs will only be shown if applicable to a given dependency:

- __"info"__, __"readme"__, and __"source"__ are applicable to all dependency types. 

- __"templateData"__ and __"tree"__ are applicable to Components. 

- __"example"__ is applicable to Component, Directive, Injectable, and Pipe dependencies.

Additionally, __"example"__, __"readme"__, and __"templateData"__ tabs will only be shown if a 
dependency specifies content for them. For instance, dependencies for which no examples are provided 
will not display an example tab.

## Example usage in a configuration file

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

## Example usage as a CLI argument

Note: Double-quotes must be escaped with "\\".

```
 compodoc --navTabConfig '[{\"id\": \"example\",\"label\": \"Overview\"},{\"id\": \"info\",\"label\": \"API\"},{\"id\": \"source\",\"label\": \"Source\"}]' -p src/tsconfig.json -n 'Documentation Name' -s
```