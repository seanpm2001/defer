# Co Defer [![Build Status](https://travis-ci.org/cojs/defer.png)](https://travis-ci.org/cojs/defer)

## API

```js
var defer = require('co-defer')
```

### var id = defer(gen, [cb])

Alias for `defer.setImmediate()`

### var id = defer.setImmediate(gen, [cb])

`gen` can be a generator or generator function. `cb` is an optional callback. If you do not set a callback, any errors will be thrown instead. `id` is returned so you can do `clearImmediate(id)`.

### defer.nextTick(gen, [cb])

Same as `setImmediate`, but with `process.nextTick`.

### var id = defer.setTimeout(gen, timeout, [cb])

Same, but with `setTimeout` and a timeout.

### var id = defer.setInterval(gen, timeout)

I think you get it.

## License

The MIT License (MIT)

Copyright (c) 2013 - 2014 Jonathan Ong me@jongleberry.com

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
