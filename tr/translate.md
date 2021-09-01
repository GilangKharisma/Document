# Çevir

## İyileştirmeler

Here is a list of improvements we are looking at making to the documentation. If you wish to contribute, try something out here:

- customise the docsify theme
- cover-page background image
- cover-page/readme gif of a terminal using One showing it's features (automatic version switching, .tool-versions with multiple runtime configs)
- custom doc site domain
- change the typography
- get a logo?
- improve "edit on GitHub" button/link
- add One to awesome-docsify showcase

## Çalışma Ortamınızı Kurun

We're using:

- [Node.js](https://github.com/One-Language/One-nodejs) `v10.15.0` to support the other required tools
- [docsify](https://docsify.js.org/#/) to create our documentation site
- [prettier](https://prettier.io/) to format our markdown files

### Install Dependencies

We are trying to **avoid polluting** the core repo with tooling for this documentation site. As such, it would be great if you could install these development tools **globally** so we don't need to commit them to this project.

```shell
npm i docsify-cli prettier -g
```

## Siteye Sunun

From the root of this repo run:

```shell
docsify serve docs
```

## Format before Committing

From the root of this repo run:

```shell
prettier --write "**/*.md"
```

## Çeviriler

It would be great to provide translations for other languages.

Docsify makes adding new languages quite easy. Look in `docs/index.html` for commented out `zh-cn` examples.

### Yeni Çeviriler Ekleme

1. create a folder in root for the new translation

   ```
   ar/
   tr/
   fa/
   en/
   de/
   se/
   ```

2. copy file from root `_404.md` to new folder `de/_404.md`

   ```
   _404.md
   de/_404.md
   ```

3. replace text with translated text.
4. repeat for all files.
5. add a link to the new translation in `_navbar.md`.
6. run `prettier` before committing.

For more information, see the [Configuration](https://docsify.js.org/#/configuration) docsify docs, the [Custom navbar](https://docsify.js.org/#/custom-navbar) docsify docs, and have a look at their own `index.html`'s [search section](https://github.com/docsifyjs/docsify/blob/6ac7bace213145cb655e9a5e9e209384db08e5f9/docs/index.html#L48).
