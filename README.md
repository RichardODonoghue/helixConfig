# My personal config for the Helix text editor

This is set up with support for formatting with Prettier, linting with ESLint, emmet and LSP configuration for Typescript, TSX, JSX, Javascript, JSON, HTML, CSS, TailwindCSS and rainbow CSV formatting. 

This setup provides a good base for anyone wanting to try the editor for web development.

# Themes 
This configuration uses the stock key mappings and has the `monokai_pro` theme enabled by default. This can be configured to something else in config.toml. 
There is a folder called themes in the repo directory which contains a collection of additional themes

# Requirements

In order to have a fully functional configuration, you will need to install the following NPM packages globally 

Run the following commands in your terminal (assuming you are running a linux distribution). 

```
npm i -g vscode-langservers-extracted prettier emmet-ls  @tailwindcss/language-server typescript-language-server typescript intelephense eslint
```

# Yazi integration
This repo contains configuration for integration the Yazi File browser with Helix.
To use this, install Yazi and Zellij
https://yazi-rs.github.io/docs/installation
https://zellij.dev/documentation/installation

The integration is setup using the below guide
https://yazi-rs.github.io/docs/installation

After this, check the health of your Helix setup by running `hx --health`

