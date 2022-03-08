# loaders
## source-map-loader
- enforce: 'pre': makes this loader run as a "pre-loader"
## oneOf
- one type of file will use **only one** of the loaders in oneOf array.
## images
- asset
## svg
- @svgr/webpack 
- file-loader
## js
- babel-loader
 - Process application JS with Babel.
 - Process any JS outside of the app with Babel.
## CSS
### style files regexes
```js
 const cssRegex = /\.css$/;
 const cssModuleRegex = /\.module\.css$/;
 const sassRegex = /\.(scss|sass)$/;
 const sassModuleRegex = /\.module\.(scss|sass)$/;
 ```
 - so we can see Recat supports CSS and SASS by defaute 
### getStyleLoaders
- step1:postcss-loader / Processing CSS Compatibility
- step2:css-lodar / Package CSS into JS
- step3:
 - development: style-lodar / Support HRM
 - production : MiniCssExtractPlugin.loader / Packaging CSS separately
## file loader: in webpack 5 is assest
- **Make sure to add the new loader(s) before the "file" loader.**

# plugins
## HtmlWebpackPlugin
- Generates an `index.html` file with the `<script>` injected.

## isEnvProduction -> pllugins for production environment
### InlineChunkHtmlPlugin
### InterpolateHtmlPlugin(HtmlWebpackPlugin, env.raw),
### ModuleNotFoundPlugin(paths.appPath),
### webpack.DefinePlugin(env.stringified),
- Defining environment variables
### MiniCssExtractPlugin
- Extract CSS into a separate file
## isEnvDevelopment -> pllugins for production environment
### CaseSensitivePathsPlugin
- File paths are case sensitive
## WebpackManifestPlugin
## useTypeScript
### ForkTsCheckerWebpackPlugin
# performance: false
