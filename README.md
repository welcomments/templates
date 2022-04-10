# Welcomments Templates & Samples

This repository contains sample Welcomments integrations for various static site generators.

## No but really, what is this stuff?

Welcomments is a comment system for static site generator based websites that pre-renders visitor comments in 100% static, prebuilt HTML. [The Welcomments website](https://welcomments.io/) has a quick run-through how Welcomments works. And [here's a YouTube video](https://www.youtube.com/watch?v=AIG7LTOrd1Q) that shows how to integrate Welcomments to a Hugo website from scratch in 1 minute and 54 seconds.

The templates in this Git repository are complete sample projects that have Welcomments already integrated. This means that if you want to see the Welcomments Jekyll integration in action, you can do `cd jekyll && bundle install && jekyll serve`.

**These templates are also the source of truth** for [the Welcomments integration wizard](https://app.welcomments.io/new/choose). This means that these exact files are used for automatically creating a pull request that integrates Welcomments to the GitHub repository of your website. This is the same integration wizard that you saw in [the YouTube video above](https://www.youtube.com/watch?v=AIG7LTOrd1Q).

## Pull request description templates

In the `_integration_instructions` directory, you will find the [Embedded Elixir](https://hexdocs.pm/eex/1.12.3/EEx.html) files that are used for the description of the automatically created GitHub pull request that integrates Welcomments to your GitHub repository.

The `common.md.eex` file defines the structure for the pull request description. Because the configuration for the static site generators differs from each other, there are also `<static site generator name>.md.eex` files that have instructions for each specific static site generator.

There are a handful of variables, denoted by `<%= variable_name %>` that will be dynamically replaced in the `.md.eex` files with appropriate values.

Available variable substitutions:

- **branch_name**: The name of the Welcomments integration Git branch.
- **specific_instructions**: The instructions specific for a single static site generator, such as Jekyll.
- **website_id**: The unique identifier for the website (generated in the Welcomments console) that identifies the website where all reader comments will be delivered to.

## Used versions

All of the templates have been tested on a macOS with an M1 chip, but should work the same on Windows and Linux.

### 11ty (Eleventy)

Tested against [v1.0.0](https://github.com/11ty/eleventy/releases/tag/v1.0.0).

### Hugo

Tested against [v0.96.0](https://github.com/gohugoio/hugo/releases/tag/v0.96.0).

### Jekyll

Tested against [v4.2.2](https://github.com/jekyll/jekyll/releases/tag/v4.2.2).
