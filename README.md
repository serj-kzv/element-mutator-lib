# Not for a production!
It is for my "home" project and it has not unit tests and it is my playground.
I strongly recommend to don't use it in production.

# Installation
```bash
npm install element-mutator-lib
```

# How to use
**Example 1.** Run after page is loaded and track all DOM changes.
```js
import ElementMutator from 'element-mutator-lib';

const elementMutator = new ElementMutator({attributeFilter: []}, (cfg, node, attributeName) => {
    // do something
    elementMutator.stop(); // stop
});
```
**Example 2.** Track a specific DOM node and all his descendants (`<body>` body tag in that case).
```js
import ElementMutator from 'element-mutator-lib';

const elementMutator = new ElementMutator({attributeFilter: [], node: document.body}, (cfg, node, attributeName) => {
    // do something
    elementMutator.stop(); // stop
});
```
**Example 3.** Track a specific DOM node attributes (`href` attribute in that case).
If `attributeName` is `undefined` then mutation is a non attribute mutation.
```js
import ElementMutator from 'element-mutator-lib';

const elementMutator = new ElementMutator({attributeFilter: [href]}, (cfg, node, attributeName) => {
    // do something
    elementMutator.stop(); // stop
});
```