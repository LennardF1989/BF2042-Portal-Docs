# BF2042 Portal Documentation
This repository provides all content for the BF2042 Portal documentation website.

## Usage

### Site structure
The site structure is determined by the directories and Markdown files in there. There is no limit to the number of subfolders and files.

### mainNavigation.json
This file contains the links in the Main Navigation block and shows on all pages. You can try to make a PR for this, but it will most likely be rejected.

### index.md
Each directory can have it's own index.md file, it will be the first page visible when someone browses into that directory.

### subNavigation.json
Each directory can have a subNavigation.json, which allows adding one or more collapsing/expanding sections in the navigation with one or more links each.

The format is as follows:
```json
[
    {
        "Title": "A title",
        "Links": {
            "Link Title": "Link URL"
        }
    }
]
```

### Markdown Files
All pages are written in Markdown and are pretty much GitHub flavored, with some additional functionality.

A "Table of Contents" is generated and shown in the navigation based on the usage of headers. For best results, use multiple `#` headers to divide a page in sections.

You can also include a code fence to render BF2042 Portal blocks. Simple copy a block using the [Browser Extension](https://github.com/LennardF1989/BF2042-Portal-Extensions), then paste it on a page as follows:

````
```blockly
<block xmlns="https://developers.google.com/blockly/xml" type="ForceRevive">
  <value name="VALUE-0">
    <block type="EventPlayer"></block>
  </value>
</block>
```
````
## First steps
With this being a new project, the first steps to take is probably to go over the original block documentation and extend them with more useful information. For example: some blocks only work if they are used together with a `Wait`-block. That's information someone needs to know about...

Generated documentation on the different events and selection lists will be added soon, those will then have to be cleaned up as well.

## Contributing
You can contribute by making Pull Requests (PR). Try making separate PR's when editing different pages, this allows us to accept smaller changes faster.