# Config Options

This page will go into more detail on the available config options that this plugin provides. 

## Option: *`version`* 

This is a **REQUIRED** option. This lets the plugin know what version the docs belong to. It is recommended that you use [semantic versioning](https://semver.org/) but any versioning scheme works. The versions are parsed as type *`str`* and is sorted alphabetically in descending order. 

???+ example "Example *`mkdocs.yml`*"
    ```yaml
    plugins:
    - mkdocs-versioning:
        version: 0.3.0
    ```

## Option: *`exclude_from_nav`* 

This is a **OPTIONAL** option. This lets the plugin know what files to exclude from the navifation. The value should be a list of paths from the *`docs`* directory.

???+ example "Example *`mkdocs.yml`*"
    ```yaml
    plugins:
    - mkdocs-versioning:
        exclude_from_nav: ["images"]
    ```

## Option: *`version_selection_page`* 

This is a **OPTIONAL** option. This lets the plugin know if there is a custom version selection page and to use rather than the default. The markdown file should be located in the *`docs`* directory

???+ example "Example *`mkdocs.yml`*"
    ```yaml
    plugins:
    - mkdocs-versioning:
        version_selection_page: "version_page.md"
    ```

## Option: *`allow_rebuild`*

This is a **OPTIONAL** option. This lets the plugin know if building a version that already exists in output directory is allowed. (Default: `False`)

???+ example "Example *`mkdocs.yml`*"
    ```yaml
    plugins:
    - mkdocs-versioning:
        allow_rebuild: True
    ```

## Option: *`nav`*

This is a **OPTIONAL** option. Nav to generate in the root *`docs`* directory. (Default: `{'Home': 'index.md'}`)

???+ example "Example *`mkdocs.yml`*"
```yaml
plugins:
- mkdocs-versioning:
    nav: 
      - Home: "index.md"
      - Project: "project.md" 
```

## Option: *`version_selection_generated_name`*

This is a **OPTIONAL** option. Customize generated name for version selection page. You should refer to this name inside 
`nav ` option. (Default: `index.md`)

???+ example "Example *`mkdocs.yml`*"
```yaml
plugins:
- mkdocs-versioning:
    version_selection_generated_name: "version-chooser.md"
```
