# slidev-theme-doli

[![NPM version](https://img.shields.io/npm/v/slidev-theme-doli?color=3AB9D4&label=)](https://www.npmjs.com/package/slidev-theme-doli)

A reproduce the ppt style of antfu's speech at viteConf2023 theme for [Slidev](https://github.com/slidevjs/slidev).

Live demo: [here](https://slidev-theme-penguin.alvarosaburido.dev/)

## Install

Add the following frontmatter to your `slides.md`. Start Slidev then it will prompt you to install the theme automatically.

<pre><code>---
theme: <b>doli</b>
---</code></pre>

It is also required to install the npm package vite-svg-loader and adding a vite.config.js in your project with the following:

```ts
import svgLoader from 'vite-svg-loader'

export default {
  plugins: [svgLoader()],
}
```

Learn more about [how to use a theme](https://sli.dev/themes/use).

## Layouts

This theme provides the following layouts:

### Configure lighting direction

Provides 8 different angles of lighting directions
> Number mapping in position matches ppt page number

```md
---
themeConfig:
 position: 
  1: right-up
  2: right-middle
  3: right-down
  4: left-down
  5: left-middle
  6: left-up
  7: top-up
  8: top-down
---
```

## Case

Start                       | End
:-------------------------:|:-------------------------:
![Start](./public/case-start.png) | ![End](./public/case-end.png)

## Thank

- https://talks.antfu.me/2023/viteconf/1
- https://antfu.me/posts/roads-to-oss-set-theory-viteconf-2023
- https://sli.dev/