# HTTP Status Codes for Express

[![npm version](https://badge.fury.io/js/http-status-code.svg)](https://www.npmjs.com/package/http-status-code)

This npm package provides a convenient way to use HTTP status codes with Express.js applications. It exports an object containing all standard HTTP status codes, making it easy to reference them in your Express routes.

### Installation

You can install the package via npm:

### bash

```sh
npm install http-status-codes-express
```

### Usage
Importing
You can import the HTTP status codes object as http:

```javascript

const http = require('http-status-codes-express');
```
Or if you're using ES6 modules:

```javascript

import http from 'http-status-codes-express';
```
### Example
Here's how you can use it in an Express route:

```javascript

const express = require('express');
const app = express();
const http = require('http-status-codes-express');

app.get('/example', (req, res) => {
// Send a 200 OK response
res.status(http.statusOk).send('This is an example route');
});

app.listen(3000, () => {
console.log('Server is running on port 3000');
});
```
### Available Status Codes
The package exports all standard HTTP status codes as properties of the http object. For example:

http.statusOk - 200
http.statusNotFound - 404
http.statusInternalServerError - 500
And many more...
Contributing
If you encounter any issues or would like to contribute to this package, feel free to open an issue or submit a pull request.

### License

This package is open source and available under the MIT License.
