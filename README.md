# gatsby-remark-vscode-shiki

Adds vscode style syntax highlighting to code blocks in markdown files using [shiki](https://github.com/shikijs/shiki).



## Install

use npm：

```shell
npm install gatsby-transformer-remark gatsby-remark-vscode-shiki shiki
```

use yarn:

```shell
yarn add gatsby-transformer-remark gatsby-remark-vscode-shiki shiki
```



## How to use

```js
// In your gatsby-config.js
plugins: [
  {
    resolve: `gatsby-transformer-remark`,
    options: {
      plugins: [
        {
          resolve: `gatsby-remark-vscode-shiki`,
          options: {
            theme: 'dark-plus' // default theme
          }
        }
      ]
    }
  }
]
```



### Theme

You can choose these theme:

css-variables、dark-plus、dracula-soft、dracula、github-dark-dimmed、github-dark、github-light、hc_light、light-plus、material-theme-darker、material-theme-lighter、material-theme-ocean、material-theme-palenight、material-theme、min-dark、min-light、monokai、nord、one-dark-pro、poimandres、rose-pine-dawn、rose-pine-moon、rose-pine、slack-dark、slack-ochin、solarized-dark、solarized-light、vitesse-dark、vitesse-light



### Line highlighting

If you want to highlight lines of code, you also need to add some additional CSS. It adds a span around lines of code with a special class `.gatsby-highlight-code-line` that you can target with styles.

For example:

```css
.gatsby-highlight-code-line {
      background-color: hsla(207, 95%, 15%, 1);
      display: block;
      margin-right: -1.3125rem;
      margin-left: -1.3125rem;
      padding-right: 1em;
      padding-left: 1.25em;
      border-left: 0.25em solid #27aa50;
}
```

You can specify the highlighted lines outside of the code block. In the following code snippet, lines 1 and 4 through 6 will get the line highlighting.

~~~text
```javascript{1,4-6}
// In your gatsby-config.js
plugins: [
  {
    resolve: `gatsby-transformer-remark`,
    options: {
      plugins: [
        `gatsby-remark-vscode-shiki`,
      ]
    }
  }
]
```
~~~

It seems like this:

```javascript{1,4-6}
// In your gatsby-config.js
plugins: [
  {
    resolve: `gatsby-transformer-remark`,
    options: {
      plugins: [
        `gatsby-remark-vscode-shiki`,
      ]
    }
  }
]
```



The plugin will continue to be updated. If you have any ideas or suggestions, can you open a issue on [GitHub]([Issues · l123wx/gatsby-remark-vscode-shiki (github.com)](https://github.com/l123wx/gatsby-remark-vscode-shiki/issues)).