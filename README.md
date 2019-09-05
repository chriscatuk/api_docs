# API Documentation

Convert OpenAPI yaml into a beautiful static documentation for your API.

## Shins Is Not Slate

Makes use of:
* https://www.npmjs.com/package/widdershins ([commit](https://github.com/Mermade/widdershins/commit/7144a4d05d736aa89379ea5c42f4ef0c0f7f6c64))
* https://github.com/mermade/shins ([commit](https://github.com/Mermade/shins/commit/ac1d5c836adb4218fc7112fd71731bb7d7a2fe51))

Clone them in ./api_docs with:
```
git clone git@github.com:Mermade/widdershins.git
git clone git@github.com:Mermade/shins.git
```

## Usage

* Generate Markup file from OpenAPI YAML
  ```
  cd widdershins
  npm install # Only the first time
  node widdershins ../my_files/example-openapi3.0.yaml -o ../shins/source/index.html.md
  ```
* Generate HTML file from Markup file
  ```
  cd ../shins
  npm install # Only the first time
  mkdir ../api_docs
  cp -R pub ../api_docs
  node shins.js --minify --output ../api_docs/index.html
  ```

You can publish `./api_docs` directory.
