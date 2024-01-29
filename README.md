# which-country-ne-10m

Get ISO 3166-1 alpha-3 country code for geographic coordinates
in node.js or browser.

Forked from the original [which-country](https://github.com/vkurchatkin/which-country) library, 
this uses Natural Earth's 10m countries database instead of the 50m one which should provide higher accuracy and support for smaller territories 
but at the cost of performance and size. 

Powered by [rbush](https://github.com/mourner/rbush) and modified
[Natural Earth 10m countries dataset](https://www.naturalearthdata.com/downloads/10m-cultural-vectors/10m-admin-0-countries/).

If you are interested in more general solution, try [which-polygon](https://github.com/mapbox/which-polygon).

# Usage

```
npm install which-country-ne-10m
```

and then:

```javascript
var wc = require('which-country-ne-10m');

// pass [lng, lat]
console.log(wc([37, 55])); // RUS
console.log(wc([-100, 40])); // USA
console.log(wc([40, -40])); // null, somewhere in Atlantic Ocean
```

#Demo

[Demo](http://minlite.github.io/which-country-ne-10m/) with leaflet and browserify

# Development

Run tests:

```
npm test
```

Generate R-tree:

```
npm run generate
```


# License

MIT
