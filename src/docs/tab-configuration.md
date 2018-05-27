# Customizing tab order and labels

The ordering of the tabs and the text used for their labels can be modified by setting the `navTabConfig`
input either as a property in a compodoc configuration file or as an argument to the `compodoc` CLI command.

The `navTabConfig` input is an array of tab configuration objects representing the superset of tabs that will 
be shown for the various dependencies in your project. The ordering of the array determines the left-to-right 
placement of the tabs in the compodoc output, and the string value of a tab object's `label` 
property determines the label displayed on the corresponding tab.

# Defining a tab

```
{
  "id": "info",
  "label": "Custom Label"
}
```

The tab id is used to determine which tab to apply the custom placement and label to. The available tab id's are:
__"info"__, __"readme"__, __"source"__, __"templateData"__, __"tree"__, and __"example"__.

# Things to be aware of

Certain tabs will only be shown if applicable to a given dependency:

- __"info"__, __"readme"__, and __"source"__ tabs are applicable to all dependency types. 

- __"templateData"__ and __"tree"__ tabs are applicable to Components. 

- The __"example"__ tab is applicable to Component, Directive, Injectable, and Pipe dependencies.

Additionally, the __"example"__, __"readme"__, and __"templateData"__ tabs will only be shown for dependencies
that specify content for them. For instance, dependencies for which no examples are provided will not have an 
example tab.

# Example usage in a configuration file

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

# Example usage as a CLI argument

Note: Double-quotes must be escaped with "\\".

```
 compodoc --navTabConfig '[{\"id\": \"example\",\"label\": \"Overview\"},{\"id\": \"info\",\"label\": \"API\"},{\"id\": \"source\",\"label\": \"Source\"}]' -p src/tsconfig.json -n 'Documentation Name' -s
```