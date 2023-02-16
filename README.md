# quil-shadowcljs-template

## rationale
The ClojureScript implementation of Quil still depends on `lein-cljsbuild` and `lein-figwheel`, which are deprecated in favor of `figwheel-main`.
However, I did not get `figwheel-main` to run and prefer `shadow-cljs` anyway for the easy integration of npm libraries.
Discussion in original repo: https://github.com/quil/quil/issues/376

## how this template was created
- `npx create-cljs-project hello-quil`
- `npm install p5`
- change `shadow-cljs.edn` to include `[quil "4.0.0"]` and simple build `:app`
- add `index.html` to add reference to quil sketch, execute main function of sketch and include `p5.js` npm dependency

## how to run it
- run `npx shadow-cljs watch app`
