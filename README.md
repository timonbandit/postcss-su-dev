# PostCSS Su Dev

[PostCSS] plugin for internal purposes.

[PostCSS]: https://github.com/postcss/postcss

```css
@critical common.css {
  .page-title {
    margin: 30px 0 28px;
    font-weight: 700;
    font-size: 36px;
  }
  
/* Unnecessary comment */

  @media (max-width: 767px) {
    .page-title {
      font-size: 26px;
      line-height: 1.1;
    }
  }
}
```

```css
  .page-title {
    margin: 30px 0 28px;
    font-weight: 700;
    font-size: 36px;
  }

  @media (max-width: 767px) {
    .page-title {
      font-size: 26px;
      line-height: 1.1;
    }
  }
```

## Usage

Check you project for existed PostCSS config: `postcss.config.js`
in the project root, `"postcss"` section in `package.json`
or `postcss` in bundle config.

If you already use PostCSS, add the plugin to plugins list:

```diff
module.exports = {
  plugins: [
+   require('postcss-su-dev'),
    require('autoprefixer')
  ]
}
```

If you do not use PostCSS, add it according to [official docs]
and set this plugin in settings.

[official docs]: https://github.com/postcss/postcss#usage
