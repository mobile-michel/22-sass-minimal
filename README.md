# Minimal Eleventy template with Sass processing
- Eleventy 2.0.1
- Sass 1.71.1
- LiquidJS template engine

## Files & folders
- `/_includes`: layouts & includes
- `/_site`: HTML output
- `/blog`: blog pages with pagination & parent link
- `/doc`: documentation pages with pagination & parent link
- `/sass`: SASS stylesheets with 6 files
- `/`: content pages with about & 404 page

## Structure
- layouts: base + default with includes
- includes: copyright + nav-footer + nav-primary + nav-secondary
- HTML5 landmarks: `header, main & footer` + `aside & section` (with `if` condition)
- navigation links with `tags: primary, secondary & footer`
- responsive layout with flexbox on header, main & footer

## Scripts
```
"watch:eleventy": "npx @11ty/eleventy --serve",
"watch:sass": "npx sass sass:_site/css --watch",
"start": "npm run watch:eleventy & npm run watch:sass",
"build": "sass sass:_site/css --style=compressed && eleventy --pathprefix '22-sass-minimal'",
"debug": "DEBUG=* eleventy"
```

## Dependencies
```
"@11ty/eleventy": "^2.0.1",
"sass": "^1.71.1"
```

## eleventy.config.js
```
eleventyConfig.addWatchTarget("./sass/");
```

## SASS design system
- reset from Andy Bell https://piccalil.li/blog/a-more-modern-css-reset/
- variables: 8 basic colors
- landmarks: flexbox for header, main & footer. Another flexbox for aside & section.
- base: HTML elements
- navigation: not responsive
- spacing for macro layout

## Special
- Github Pages