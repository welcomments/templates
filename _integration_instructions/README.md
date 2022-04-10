# Pull request description templates

Here you will find the Markdown files that are used for the description of the automatically created GitHub pull request that integrates Welcomments to your GitHub repository.

The `common.md` file defines the structure for the pull request description. Because the configuration for the static site generators differs from each other, there are also `<static site generator name>.md` files that have instructions for each specific static site generator.

There are a handful of variables, denoted by `<%= variable_name %>` that will be dynamically replaced in the `.md` files with appropriate values.

Available variable substitutions:

- **branch_name**: The name of the Welcomments integration Git branch.
- **website_id**: The unique identifier for the website (generated in the Welcomments console) that identifies the website where all reader comments will be delivered to.
- **specific_instructions**: The instructions specific for a single static site generator, such as Jekyll.
