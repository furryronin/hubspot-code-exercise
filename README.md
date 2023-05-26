# HubSpot Web Team Exercise - Response

Details of the process and included libraries, etc have been included in the submission.md, this readme has been included to pull together the information specific to installation and operation.

# Build System: Well Meaning Webpack Workflow

A basic Webpack build process for developing static HTML websites and applications. All comments welcome.

Link -> https://github.com/furryronin/Well-Meaning-Webpack-Workflow

## Features

- Write SCSS and modern JavaScript code in `src` and build minified, transpiled code for production in `dist`
- Live reloading with webpack-dev-server
- ES6+ to ES5 transpilation, bundling, and minification
- SCSS to CSS transpilation, bundling, autoprefixing, and minification
- Automatic copying of HTML and static assets from `src` to `dist` folders
- Linting for styles and scripts
- A template engine (Handlebars)
- Import and install Javascript files 
- Custom Fonts

## Installation

Installs with the package manager of your choice, for instance node or yarn

`npm install`

or

`yarn install`

## Usage

- Write all your ES2015+ Javascript code in `src/js` and SCSS styling in `src/style`. Store static assets in `src/static`. Organize HTML files the way you like.
- Available commands:
  - `npm run build`: Build files to the `dist` folder. Transpiles down to ES5 and bundles all JS into `app.bundle.js`. Transpiles SCSS to CSS and adds prefixing into `style.bundle.css`. Copies static assets and HTML over, and bundled CSS and JS gets added to HTML file.
  - `npm run start:dev`: Runs `webpack-dev-server` at `localhost:9000`. Includes live reloading on any Javascript/SCSS/HTML changes.
  - `npm run start`: Builds files and runs a local production server on `localhost:8080` with `http-server`.
  - `npm run run lint:js`: Lints JS with ESLint.
  - `npm run lint:styles`: Lints SCSS stylesheets with stylelint.
  - `npm run lint:html`: Lints HTML for a11y issues using pa11y, performs a  fresh build runs on the dist folder to check your work.

## Filter System

# Filter.js

__A really really simple pure-Javascript class filtering script.__

Link -> https://github.com/furryronin/filter.js

Basic Setup
---------------------------

Define the filter buttons
```
<a href="#" id="filter-button-xsmall">X Small</a>
...
```
Register buttons to a filter group
```javascript
var filter = new Filter({
    'filters': [
        {
            'key': 'size', // Required, unique
            'buttons': [
                {
                    'element': document.getElementById('filter-button-xsmall'), // The filter button
                    'tag': 'xsmall' // The class you want to hide/show
                },
                ...
            ]
        }
        ...
    ]
})
```

Choose how you show/hide
```css
.filter-item-active {
    display:block;
}
.filter-item-inactive {
    display:none;
}
```

___Multiple/ Single Selection___

Allow only one filter button to be selected at a time (within a filter group)
```javascript

var filter = new Filter({
    'filters': [
        {
            'select': 'single', // Default: `multiple`
            'buttons': [],
            ...
        }
        ...
    ]
})
```

___Exclusive/Inclusive___

Change the filter type

this OR this = exclusive

this AND this = inclusive
```javascript

var filter = new Filter({
    'filters': [
        {
            'type': 'inclusive', // Default: `exclusive`
            'buttons': [],
            ...
        }
        ...
    ]
})
```

___Clear Button___

Add a button to clear the filter, the same clear button can be applied to multiple filters

```javascript

var filter = new Filter({
    'filters': [
        {
            'clear': document.getElementById('clear-button'),
            'buttons': [],
            ...
        }
        ...
    ]
})
```

___Deep Linking___

To deep link you must first generate a string

Single filter group:`key=tag1,tag2`

Multiple filter groups:`key=tag1,tag2&key2=tag1,tag2`

Then base64 encode and append to url with parameter key of `filter`:
```
?filter=a2V5PXRhZzEsdGFnMg==

// '?filter=' + bota('key=tag1,tag2')

```

___Auto generating filters___

Sometimes you will want to generate the filters from the content. 

This can be done by either using classes set on the content or in a data attribute.

_Classes_

To generate the filters, simply provide the `buttonHolder` attribute and classes to the filter items. This will tell the library where to put the list of filters. Each class you would like to generate a filter from must be prefixed with `tag-`

You also need to add `filter-item` dom element that you want to filter on.
```
<div class="filter-item tag-green tag-medium"></div>
```
```javascript


var filter = new Filter({
        'emptyBlock': document.getElementById('filter-items-empty'),
        'filters': [
            {
                ...
                'buttonHolder': document.getElementById('filterHolder')
            }
        ]
    })
```

_Attributes_
If you would prefer not to use classes you may use attributes. First add the attributes to any dom element you want to filter and reference the tag you used.
```
<div data-tags="small green"></div>
```
```javascript


var filter = new Filter({
        'emptyBlock': document.getElementById('filter-items-empty'),
        'filters': [
            {
                'attribute': 'data-tags',
                'buttonHolder': document.getElementById('filterHolder')
            }
        ]
    })
```
## Bundled Libraries

Many thanks to the awesome work done by <a href="https://github.com/browserstate" title="Link to browserstate githunb page">https://github.com/browserstate</a> and <a href="https://github.com/davidchambers/" title="Link to davidchambers githunb page">https://github.com/davidchambers</a> for the following code I've borrowed for features;

 - <a href="https://github.com/browserstate/history.js/" title="Link to history.js github page">https://github.com/browserstate/history.js/</a>

 - <a href="https://github.com/davidchambers/Base64.js/" title="Link to base64.js github page">https://github.com/davidchambers/Base64.js/</a>
