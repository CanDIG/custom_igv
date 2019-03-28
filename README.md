# custom_igv
A repo that has several igv.js that are custom to our APIs

## To develop

* Make sure you local node packages are recent enough (8+) to run babel
* `npm install @babel/preset-env --save-dev` 
* `npm install babel-minify --save-dev`.

* After changes are made, run `npx babel src --watch --out-dir dist` to minify the file, `--watch` flag is optional.

## TODO

* Document the version changes.
* Update the igv.js to the later versions.
* Clearly document the changes that are needed for the CanDIG APIs for the ease of future devs.

## FAQ

* Q: How is this different from the official igv.js?
* A: It includes a number of modifications that is custom to the APIs on CanDIG server.

* Q: Why do I need to use .babelrc to minify?
* A: Since minify has `mangle` enabled by default, which might cause unexpected errors. Babel CLI isn't particular friendly in further config in its packages through cli parameters, so using the .babelrc is a better option here.

* Q: Babel.js complains about Couldn't find intersection.
* A: Specify `"builtIns": false,` in your `.babelrc`.
