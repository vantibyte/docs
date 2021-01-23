# Vantibyte Docs

Welcome to the GitHub repository for the Vantibyte Docs site!

You probably want to see this on the web at https://docs.vantibyte.com

If you're here to help contribute to the docs, great! Feel free to open a PR on the relevant files, and if it's suitable we'll get it merged in.
If you want to run this site locally, set up a local Jekyll site with the latest `github-pages` gem and you should be good to go.

## Translations

Translations to other languages are absolutely appreciated, and can be created by copying the `en` directory and updating each of the markdown files with their translated equivalent. The `_config.yml` file will additionally require a new defaults entry to apply the language code to the directory (see the bottom of the file for examples). The name of the directory and entry in the config should be the internationally recognised two-letter language code.

The `lang_ref` attribute in the frontmatter should not be changed, as this is used to link together the alternate translations automatically, however the Title and Description should be localised.

Localised screenshots should be stored under `/lang/assets` as they can then be referenced in the markdown via `../assets/`. English screenshots will remain in `/assets` as a fallback for all languages.
