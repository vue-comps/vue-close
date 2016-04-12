# vue-close

A button which dispatches a close event.

### [Demo](https://vue-comps.github.io/vue-close)


# Install

```sh
npm install --save-dev vue-close
```
or include `build/bundle.js`.

## Usage
```coffee
# in your component
components:
  "close": require("vue-close")
# or, when using bundle.js
components:
  "close": window.vueComps.close
```
```html
<close>Dismiss</close>
```
content defaults to "Close"

For examples see [`dev/`](dev/).

#### Events
| Name |  description |
| ---:| --- | ---| --- |
| before-close |  will be emitted before close is dispatched |
| close |  will be dispatched on click |

# Development
Clone repository.
```sh
npm install
npm run dev
```
Browse to `http://localhost:8080/`.

## License
Copyright (c) 2016 Paul Pflugradt
Licensed under the MIT license.
