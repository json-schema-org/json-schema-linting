[Spectral](https://stoplight.io/open-source/spectral) is a linting tool for JSON and YAML.

It's most used to help developers make informed decisions when composing OpenAPI and AsyncAPI documents.

This folder supplies a ruleset that can do the same for JSON Schema in general.

Spectral works by defining a set of rules.  The rules defining herein work independently of each other and typically focus on a single problem or area.

For more information on how Spectral rules work, you can read their [full documentation](https://docs.stoplight.io/docs/spectral/).

## Using the ruleset

Currently the rules are only published as part of this repository, however we are exploring other publication options.

To use these rules, first clone this repository.

You can run the CLI linter (downloadable separately) from this folder (_./spectral_).  Check the CLI documentation for more options and configuration.

### In Visual Studio Code

If you're a VSCode user, Spectral offers an extension.  There are a couple gotchas with using it, though.

- It expects the .spectral.yml file to be at the root of the workspace, so you may need to copy these files into the root folder of wherever your JSON/YAML files are and open _that folder_ (not a parent) in VSCode.
- You'll need to configure the extension to ignore **/*.spectral.yml files so that it doesn't try to validate the rule files themselves.

Once that's set up, you'll get problems reported in the Problems pane.