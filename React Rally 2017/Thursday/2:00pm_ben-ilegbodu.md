# Ben Ilegbodu

## With React 16:

- React Fiber
    - Rewrite of reconciler
    - Prioritizes UI updates
    - See [Lin Clark video](https://www.youtube.com/watch?v=ZCuYPiUIONs)

- React packages are much smaller

- Deprecations are now errors

- Adjacent elements are still errors, but we can return arrays

```
const Foo = () => ([
    (<Foo />),
    (<Bar />),
])
```

(Also see https://github.com/gajus/react-aux)

- New error handling
    - no more semi-broken pages and console errors. unmounts component instead
    - uses error bounderies

- Server Side Rendering
    - s/ReactDOM.render/ReactDOM.hydrate/
    - no more react data-ids
    - big perf benefits
    - Streaming support

    ```
    import {renderToNodeStream} from 'react-dom/server'

    app.get('/', (req, res) => {
      // write opening <html>, <head>, <body> tags streamed

      renderToNodeStream(<App />)
        .pipe(res)
        .on('end', () => {
          // write rest of page, <body>, <html>
          res.end()
        })
    })
    ```