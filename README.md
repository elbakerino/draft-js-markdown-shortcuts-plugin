draft-js-md-keyboard-plugin
==================================

- **this is a modified fork of [draft-js-md-keyboard-plugin](https://www.npmjs.com/package/draft-js-md-keyboard-plugin)**
- **supporting DraftJS ~0.11 and draft-js-plugins-editor ^2.0.4 with React ^16.2**

A [DraftJS] plugin for supporting Markdown syntax shortcuts

This plugin works with [DraftJS Plugins] wrapper component.

![screen](screen.gif)

[View Demo][Demo]

Usage
-----

```sh
npm i --save draft-js-md-keyboard-plugin
```

then import from your editor component

```js
import createMarkdownShortcutsPlugin from 'draft-js-md-keyboard-plugin';
```

Example
-------

```js
import React, { Component } from 'react';
import Editor from 'draft-js-plugins-editor';
import createMarkdownShortcutsPlugin from 'draft-js-md-keyboard-plugin';
import { EditorState } from 'draft-js';

const plugins = [
  createMarkdownShortcutsPlugin()
];

export default class DemoEditor extends Component {

  state = {
    editorState: EditorState.createEmpty(),
  };

  onChange = (editorState) => {
    this.setState({
      editorState,
    });
  };

  render() {
    return (
      <Editor
        editorState={this.state.editorState}
        onChange={this.onChange}
        plugins={plugins}
      />
    );
  }
}
```

License
-------

MIT. See [LICENSE]

[Demo]: https://ngs.github.io/draft-js-md-keyboard-plugin
[DraftJS]: https://facebook.github.io/draft-js/
[DraftJS Plugins]: https://github.com/draft-js-plugins/draft-js-plugins
[LICENSE]: ./LICENSE
[npm]: https://www.npmjs.com/package/draft-js-md-keyboard-plugin

## Contributors

This project exists thanks to all the people who contribute. [[Contribute](CONTRIBUTING.md)].
