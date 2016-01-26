# DS-GA 1003 Website

## Development info

### Building locally: quickstart

Be sure to have [Node.js](https://iojs.org/) 5.x+ installed.

Run `npm install` in the project root. This will install some build tools we use.

Run `npm run watch` to start a watcher that will compile things in place. You can then view the site by simply opening `index.html`.

Run `npm run build` to do a local build into the `out/` directory. You can then preview the site at `out/index.html`. This should usually be the same as just `index.html`, but it is good to check before committing, since the build process is slightly more complicated than the in-place watch process.

### Technologies used

[Stylus](https://learnboost.github.io/stylus/) is used for styling.

[Handlebars](http://handlebarsjs.com/) is used for templating. `index.hbs` is minimally templated, mostly delegating to the partials in `templates/`. Those pull their data from `data/`. The logic that ties them all together is in `build/templater.js`.

[Gulp](http://gulpjs.com/) is used for a build/watch system. This is abstracted behind npm tasks though (`npm run watch`, `npm run build`).

[Traceur](https://github.com/google/traceur-compiler) is used to write ES2015 code instead of boring-old-JavaScript, for the build code at least.

[Travis](https://travis-ci.org/) is used to build and deploy the website to gh-pages on each push, per [this guide](https://gist.github.com/domenic/ec8b0fc8ab45f39403dd).

The site is intended to be responsive, which we accomplish with per-device stylesheets and media queries in the HTML.

### Things to Keep in Mind

While editing you should be using an [EditorConfig](http://editorconfig.org/) plugin for your text editor to enforce a few basic stylistic things.

We are trying to maintain a reasonable HTML document outline (so, don't use `<section>` as if it were `<div>`). To preview the document outline, use the [HTML 5 Outliner tool](https://gsnedders.html5.org/outliner/); here's [a direct link to the outline for the current version](https://gsnedders.html5.org/outliner/process.py?url=https%3A%2F%2Fdavidrosenberg.github.io%2Fml2015%2F%23home).
