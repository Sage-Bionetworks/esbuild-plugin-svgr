# esbuild-plugin-svgr

A plugin for [esbuild](https://github.com/evanw/esbuild) that adds support for `*.svg` file imports as React components. This is a fork of [kazijawad/esbuild-plugin-svgr](https://github.com/kazijawad/esbuild-plugin-svgr) and is built on top of [SVGR](https://github.com/gregberge/svgr).

## Basic Usage

1. Install the plugin in your project:
```bash
npm install --save-dev @sage-bionetworks/esbuild-plugin-svgr
# or use yarn
yarn add --dev @sage-bionetworks/esbuild-plugin-svgr
```

2. Add this plugin to your esbuild build script:
```js
const svgrPlugin = require('@sage-bionetworks/esbuild-plugin-svgr');

esbuild.build({
    plugins: [
        svgrPlugin(),
    ],
});
```

3. Import your `*.svg` file from JavaScript:
```js
import Icon from './icon.svg';

function App() {
    return (
        <div>
            <Icon />
        </div>
    );
}
```

4. Pass in optional [supported](https://react-svgr.com/docs/options/) configuration options:
```js
esbuild.build({
    plugins: [
        svgrPlugin({ ref: true }),
    ],
});
```

## Author

This fork is maintained by [Sage Bionetworks](https://sagebionetworks.org/). Originally by [Kazi Jawad](https://github.com/kazijawad).

## License

This project is licensed under the MIT License - see the [LICENSE.md](https://github.com/Sage-Bionetworks/esbuild-plugin-svgr/blob/main/LICENSE.md) file for details.

## Acknowledgements

[SVGR](https://github.com/gregberge/svgr)
