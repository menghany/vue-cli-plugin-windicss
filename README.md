<h1 align='center'>vue-cli-plugin-windicss</h1>

<p align='center'><a href="https://github.com/windicss/windicss">Windi CSS</a> for Vue CLI, it's fast! ⚡️<br>
<sup><em>a.k.a On-demand Tailwind CSS</em></sup>
</p>

<p align='center'>
<a href='https://www.npmjs.com/package/vue-cli-plugin-windicss'>
<img src='https://img.shields.io/npm/v/vue-cli-plugin-windicss?color=0EA5E9&label='>
</a>
</p>

<p align='center'>
<a href='https://twitter.com/antfu7/status/1361398324587163648'>⚡️ See speed comparison with Tailwind</a>
</p>

## Features

- ⚡️ **It's FAST** - 20~100x times faster than [vue-cli-plugin-tailwind](https://github.com/forsartis/vue-cli-plugin-tailwind)
- 🧩 On-demand CSS utilities (Compatible with Tailwind CSS v2) and native elements style resetting
- 🍃 Load configurations from `tailwind.config.js`
- 📄 Use `@apply` / `@screen` directives in any file: Vue SFC, Less, SCSS, SASS, PostCSS, Stylus
- 🎳 Support Utility Groups - e.g. `bg-gray-200 hover:(bg-gray-100 text-red-300)`

## Setup

Install using Vue CLI. (Vue CLI 4+ is recommended)

```bash
vue add windicss
```

### Import

Make sure the import for Windi CSS is within your `main.js` file, the above should do it for you.

```
import 'windi.css'
```

## Configuration

You can change the behaviour of the plugin by modifying the options in `./vue.config.js`.

```js
// vue.config.js
module.exports = {
  pluginOptions: {
    windicss: {
      // see https://github.com/windicss/vite-plugin-windicss/blob/main/packages/plugin-utils/src/options.ts
    }
  }
}
```

If you have a `tailwind.config.js`, please rename it to `windi.config.js` or `windi.config.ts`.

See [here](https://windicss.netlify.app/guide/configuration.html) for configuration details.


## Migrating

If you were previously using `vue-cli-plugin-tailwind`, please consult the [documentation](https://windicss.netlify.app/guide/migration.html) on migrating.

```bash
yarn remove vue-cli-plugin-tailwind
```

## Configuration

- Default:
```js
export default {
  scan: {
    dirs: ['src', 'public'],
    exclude: [
      'node_modules',
      '.git',
    ],
    include: []
  },
}
```  

- See [options.ts](https://github.com/windicss/vite-plugin-windicss/blob/main/packages/plugin-utils/src/options.ts) for configuration reference.

### Examples

#### Disable Preflight

_vue.config.js_
```js
module.exports = {
  // ...
  pluginOptions: {
    windicss: {
      preflight: false,
    }
  }
}
```

## Credits

- [Windy CSS team](https://github.com/windicss) 

## Sponsors

<p align="center">
  <a href="https://raw.githubusercontent.com/harlan-zw/static/main/sponsors.svg">
    <img src='https://raw.githubusercontent.com/harlan-zw/static/main/sponsors.svg'/>
  </a>
</p>

## License

MIT License © 2021 [Harlan Wilton](https://github.com/harlan-zw)

