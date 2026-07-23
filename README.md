# eaydin-dev.github.io

Personal website built with Hugo and the Terminal theme.

## Local development

Clone the repository with its theme submodule, then run Hugo:

```sh
git submodule update --init --recursive
hugo server
```

Create a production build with:

```sh
hugo --cleanDestinationDir --gc --minify
```

Pushing to `main` runs the GitHub Pages workflow and publishes the generated
site to the `gh-pages` branch.
