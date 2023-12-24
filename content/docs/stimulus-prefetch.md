---
title: Prefetch
description: A Stimulus controller that prefetch in-viewport links.
package: prefetch
---

## Installation

```bash
$ yarn add stimulus-prefetch
```

And use it in your JS file:

```js
// Probably in app/javascript/controllers/index.js

import { Application } from '@hotwired/stimulus'
import Prefetch from 'stimulus-prefetch'

const application = Application.start()
application.register('prefetch', Prefetch)
```

:demo-link{package-name="prefetch"}

## Usage

```html
<a href="/about" data-controller="prefetch">About</a>.
```

**Note**: To improve performance, links will only be prefetched if they are in the viewport and if the user isn't on a slow connection.

## 🎛 Extending Controller

::extending-controller

```js
import Prefetch from 'stimulus-prefetch'

export default class extends Prefetch {
  connect() {
    super.connect()
    console.log('Do what you want here.')
  }
}
```

::
