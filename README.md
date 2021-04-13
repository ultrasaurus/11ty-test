
# 11ty test site

This is just a sample blog / website to experiment with 11ty


## Steps to re-create
set up git repo, copy .gitignore from
 https://github.com/github/gitignore/blob/master/Node.gitignore
 plus 
 ```
 _site/
 ```

install
 ```
 npm install -g local-web-server
```

then on command line...
```
yarn init 
yarn add @11ty/eleventy
```

to generate the site:
```
npx @11ty/eleventy
```
or preview...
```
npx @11ty/eleventy --serve
```

## Notes

Mustache because
https://css-tricks.com/killer-features-of-nunjucks/
Nunjucks calls itself “A rich and powerful templating language for JavaScript”, which sounds about right. It’s not intentionally super lightweight like Mustache or the slightly more robust (but still pretty light) Handlebars. It’s a full-on language, packed with all kinds of stuff you might want when writing templates.

could find zero tutorials using mustache, so starting with Nunjucks (.njk)


https://24ways.org/2018/turn-jekyll-up-to-eleventy/

* "Whereas Jekyll uses the declarative YAML syntax for its configuration file, Eleventy uses JavaScript." ```.eleventy.js```
* excludes files in `.eleventyignore` (in addition to `.gitignore`)
* By default, Eleventy uses [markdown-it](https://github.com/markdown-it/markdown-it) to parse Markdown. If your content uses advanced syntax features (such as abbreviations, definition lists and footnotes), you’ll need to pass Eleventy an instance of this (or another) Markdown library configured with the relevant options and plugins, see [11ty markdown options](https://www.11ty.dev/docs/languages/markdown/)


borrowed post & base template inspiration from [eleventy-base-blog](https://github.com/11ty/eleventy-base-blog/blob/master/_includes/layouts/post.njk)