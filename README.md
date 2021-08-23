gridsome-plugin-remark-emoji
============
[![CI][ci-badge]][ci]
[![npm][npm-badge]][npm]

This is a [remark](https://github.com/remarkjs/remark) plugin to replace `:emoji:` to real UTF-8 emojis in text. 

It's a modification of `remark-emoji` that strips out all ESM-only dependencies, and allows it to be used with Gridsome as a plugin of `gridsome-plugin-remark-container`.

## Demo

You can find a demo in the following [Codesandbox](https://codesandbox.io/s/remark-emoji-example-osvyi).

## Usage

In your `gridome.config.js`:

```javascript
 transformers: {
    remark: {
      externalLinksTarget: "_blank",
      externalLinksRel: ["nofollow", "noopener", "noreferrer"],
      anchorClassName: "icon icon-link",
      plugins:  ["gridsome-plugin-remark-container",
                'gridsome-plugin-remark-emoji']
    }
```

## Options

### `options.padSpaceAfter`

Setting to `true` means that an extra whitespace is added after emoji.
This is useful when browser handle emojis with half character length and following character is hidden.
Default value is `false`.

### `options.emoticon`

Setting to `true` means that [emoticon](https://www.npmjs.com/package/emoticon) shortcodes are supported (e.g. :-) will be replaced by 😃).
Default value is `false`.

## License

Distributed under [the MIT License](LICENSE).



[ci-badge]: https://github.com/rhysd/remark-emoji/workflows/CI/badge.svg?branch=master&event=push
[ci]: https://github.com/rhysd/remark-emoji/actions?query=workflow%3ACI
[npm-badge]: https://badge.fury.io/js/remark-emoji.svg
[npm]: https://www.npmjs.com/package/gridsome-plugin-remark-emoji
