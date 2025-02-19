# re:Clojure

This repo contains the website for https://reclojure.org

## Development

CLI commands listed below should be run from the project’s root.

Also, make sure you have done `npm install` at least once.

### Emacs and Cider setup

Run `cider-jack-in-clj&cljs` and then eval `(go)` at the REPL to start
the development http server at http://localhost:7070

## Build

To build the project, run the following command:

```
make build
```

This command creates and populates the `docs` directory with the
result of running the build process merged with the files that are in
`resources/public`. `docs` is the directory that should be published.

## Local server to inspect build results

To test the output of the build process locally before deploying, run
a local dev server with `make server` and visit `localhost:8080`.

Note that this currently uses Python 3, but from within `docs`, any
other local web server will probably do.

## Deploy

Merge the project with the generated output into master and it will be
published live.

## Cleanup

After the build is created and deployed, make sure to run `make clean`
if you branch from master in order to resume development, otherwise
the CSS generated by the build process will stop newer CSS from
loading.
