# react-tiny-dom (WIP)

`react-tiny-dom` is a minimal implementation of [react-dom](https://reactjs.org/docs/react-dom.html) as custom renderer using React 16 official Renderer API.

The purpose of this project is to show the meaning of each method of the `ReconcilerConfig` passed to [react-reconciler](https://github.com/facebook/react/tree/master/packages/react-reconciler), by using a practical yet familiar environment: the browser DOM.

## What's supported

- Nested React components
- Text nodes
- HTML Attributes
- `className` attribute
- `setState` with updates on Text Nodes or HTML attributes

## What's not supported yet

- Event Listener props
- `style` attribute
- Web Components

## Installation

```
npm install
npm start # Runs the example using react-tiny-dom
```

## FAQ

### How can I avoid the logging of some methods?

By default the demo logs every method call of the Renderer, but you can pass a list of method names to avoid in the second parameter of `debugMethods`, when passing the `ReconcilerConfig` to `Reconciler`.

```js
const TinyDOMRenderer = Reconciler(
  debugMethods(hostConfig, ['now', 'getChildHostContext', 'shouldSetTextContent'])
);
```
