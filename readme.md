[![NPM](https://nodei.co/npm/metalsmith-inspect-files.png)](https://npmjs.org/package/metalsmith-inspect-files)
## metalsmith inspect files

This is metalsmith plugin that prints files tree in selected build step.

Example with printing build result:
```javascript
const Metalsmith = require('metalsmith');
const metalsmithInspectFiles = require('metalsmith-inspect-files');

Metalsmith(__dirname)
    .source('./source')
    .destination('./build')
    .clean(true)
    .use(metalsmithInspectFiles())
    .build((err, files) => {
        if (err) { throw err; }
    });

```