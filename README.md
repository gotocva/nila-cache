### Nila in memory cache

## Installation

```bash
npm install nila-cache --save
```

## Usage

```javascript
const cache = require('nila-cache');

// now just use the cache

cache.store('name', 'sivabharathy');
console.log(cache.get('foo'));

// that wasn't too interesting, here's the good part
cache.store('houdini', 'disappear', 100, function(key, value) {
    console.log(key + ' did ' + value);
}); // Time in ms

// create new cache instance
const newCache = new cache.NilaCache();

newCache.store('name', 'gotocva');

setTimeout(function() {
  console.log('name in old cache is ' + cache.get('foo'));
  console.log('name in new cache is ' + newCache.get('foo'));
}, 200);
```

