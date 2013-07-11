# piped npm mcp

a pipe-friendly `npm run`

npm has `npm run` which is kind of a helmsman for package.json rather than js, an index service for registering subprograms. it's pretty handy but it also outputs a bunch of noisy stuff too pertaining to npm, and there doesn't seem to be a native way to make it quiet-like. `pnm` is an alias to `npm run` but which does not emit this verbose information.

# howto

`npm install -g pnm` to install. from now on, where you'd type `npm run` you can go `pnm` instead.

# comparison

## using npm run

```$ npm run many-err

> pnm@1.0.0 many-err /home/rektide/archive/pnm
> echo stderr1 >&2; echo stderr2 >&2; echo stderr3 >&2; echo stdout; echo stderr4 >&2

stderr1
stderr2
stderr3
stdout
stderr4```

## using pnm

```$ pnm many-err

stderr1
stderr2
stderr3
stdout
stderr4```
