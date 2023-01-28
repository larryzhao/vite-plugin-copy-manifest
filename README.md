# vite-plugin-copy-manifest

Copies the manifest.json file generated by `vite build` to a specific location.

Vite will generate a manifest json file after `vite build`, will always generate this file inside `build.outDir`, there's no configuration to change the destination dir for the generation of the manfest file. Sometimes you need this manifest file in a specific location. You could use this plugin to copy the generated manifest file to the destination location you specified.

# Install
```bash
npm i vite-plugin-copy-manifest -D
```

# Usage
```javascript
import copyManifest from 'vite-plugin-copy-manifest';

export default {
  build: {
    manifest: "assets.json",
    outDir: "./static/dist/",
  },
  plugins: [
    // specify destDir
    // the manifest file `assets.json` will be copied to `./data/`
    copyManifest({ destDir: './data/' })
  ]
}
```

# License
MIT License © 2023-PRESENT [@larryzhao](https://github.com/larryzhao)