# falcon-listr-update-renderer

> Note: This renderer is based on v0.4.0 of the original [listr-update-renderer](https://github.com/SamVerschueren/listr-update-renderer), created by Sam Verschueren.


## Install

```
$ npm install --save falcon-listr-update-renderer
```


## Usage

```js
const FalconUpdaterRenderer = require('falcon-listr-update-renderer');
const Listr = require('listr');

const list = new Listr([
    {
        title: 'foo',
        task: () => Promise.resolve('bar')
    }
], {
    renderer: FalconUpdaterRenderer,
	collapse: false
});

list.run();
```


## Options

These options should be provided in the [Listr](https://github.com/SamVerschueren/listr) options object.

### showSubtasks

Type: `boolean`<br>
Default: `true`

Set to `false` if you want to disable the rendering of the subtasks. Subtasks will be rendered if an error occurred in one of them.

### collapse

Type: `boolean`<br>
Default: `true`

Set to `false` if you don't want subtasks to be hidden after the main task succeed.

### clearOutput

Type: `boolean`<br>
Default: `false`

Clear the output when all the tasks are executed succesfully.


## Related

- [listr](https://github.com/SamVerschueren/listr) - Terminal task list
- [listr-update-renderer](https://github.com/SamVerschueren/listr-update-renderer) - Original update renderer
- [listr-verbose-renderer](https://github.com/SamVerschueren/listr-verbose-renderer) - Listr verbose renderer
- [listr-silent-renderer](https://github.com/SamVerschueren/listr-silent-renderer) - Suppress Listr rendering output