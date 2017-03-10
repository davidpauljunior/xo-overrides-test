# Tests 'overrides' option in XO when used from CLI

XO is the only dependency

`npm install`

Default options are set to `"space": 2` and `"envs": ["node"]`.

Overrides are set to `"files": "index.js"`, `"space": 4` and `"envs": ["browser"]`.

Expecting to see no errors reported for the following code inside `index.js`:

```
if (document) {
    console.log('test');
}
```

But see errors:

`document is not defined.`

`Expected indentation of 2 spaces but found 4.`