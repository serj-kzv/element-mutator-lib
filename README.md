# Not for a production!
It is my for my "home" project and it has not unit tests and it is my playground.
I strongly recommend to don't use it in production.

# How to use
**Example 1.** Run after page is loaded and track all DOM changes.
```js
const elementMutator = new ElementMutator({attributeFilter: []}, (cfg, node, attributeName) => {
    // do something
    elementMutator.stop(); // stop
});
```
**Example 2.** Track a concreate DOM node and all his descendants.
```js
const elementMutator = new ElementMutator({attributeFilter: [], node: document.body}, (cfg, node, attributeName) => {
    // do something
    elementMutator.stop(); // stop
});
```
**Example 3.** Track a concreate DOM node attributes.
If `attributeName` is `undefined` then mutation is a non attribute mutation.
```js
const elementMutator = new ElementMutator({attributeFilter: [href]}, (cfg, node, attributeName) => {
    // do something
    elementMutator.stop(); // stop
});
```