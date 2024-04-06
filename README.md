# HTTP Status Codes for Express

[![npm version](https://badge.fury.io/js/response-status-code.svg)](https://www.npmjs.com/package/response-status-code)

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
const http = require("http-status-codes-express");
```

Or if you're using ES6 modules:

```javascript
import http from "http-status-codes-express";
```

### Example

Here's how you can use it in an Express route:

```javascript
const express = require("express");
const app = express();
const http = require("http-status-codes-express");

app.get("/example", (req, res) => {
  // Send a 200 OK response
  res.status(http.statusOk).send("This is an example route");
});

app.listen(3000, () => {
  console.log("Server is running on port 3000");
});
```

### Available Status Codes

The package exports all standard HTTP status codes as properties of the http object. For example:

| Status Code | Description                     | Function Call                            |
| ----------- | ------------------------------- | ---------------------------------------- |
| 100         | Continue                        | `http.statusContinue`                    |
| 101         | Switching Protocols             | `http.statusSwitchingProtocols`          |
| 102         | Processing                      | `http.statusProcessing`                  |
| 103         | Early Hints                     | `http.statusEarlyHints`                  |
| 200         | OK                              | `http.statusOk`                          |
| 201         | Created                         | `http.statusCreated`                     |
| 202         | Accepted                        | `http.statusAccepted`                    |
| 203         | Non-Authoritative Information   | `http.statusNonAuthoritativeInformation` |
| 204         | No Content                      | `http.statusNoContent`                   |
| 205         | Reset Content                   | `http.statusResetContent`                |
| 206         | Partial Content                 | `http.statusPartialContent`              |
| 207         | Multi-Status                    | `http.statusMultiStatus`                 |
| 208         | Already Reported                | `http.statusAlreadyReported`             |
| 226         | IM Used                         | `http.statusIMUsed`                      |
| 300         | Multiple Choices                | `http.statusMultipleChoices`             |
| 301         | Moved Permanently               | `http.statusMovedPermanently`            |
| 302         | Found                           | `http.statusFound`                       |
| 303         | See Other                       | `http.statusSeeOther`                    |
| 304         | Not Modified                    | `http.statusNotModified`                 |
| 305         | Use Proxy                       | `http.statusUseProxy`                    |
| 307         | Temporary Redirect              | `http.statusTemporaryRedirect`           |
| 308         | Permanent Redirect              | `http.statusPermanentRedirect`           |
| 400         | Bad Request                     | `http.statusBadRequest`                  |
| 401         | Unauthorized                    | `http.statusUnauthorized`                |
| 402         | Payment Required                | `http.statusPaymentRequired`             |
| 403         | Forbidden                       | `http.statusForbidden`                   |
| 404         | Not Found                       | `http.statusNotFound`                    |
| 405         | Method Not Allowed              | `http.statusMethodNotAllowed`            |
| 406         | Not Acceptable                  | `http.statusNotAcceptable`               |
| 407         | Proxy Authentication Required   | `http.statusProxyAuthenticationRequired` |
| 408         | Request Timeout                 | `http.statusRequestTimeout`              |
| 409         | Conflict                        | `http.statusConflict`                    |
| 410         | Gone                            | `http.statusGone`                        |
| 411         | Length Required                 | `http.statusLengthRequired`              |
| 412         | Precondition Failed             | `http.statusPreconditionFailed`          |
| 413         | Payload Too Large               | `http.statusPayloadTooLarge`             |
| 414         | URI Too Long                    | `http.statusURITooLong`                  |
| 415         | Unsupported Media Type          | `http.statusUnsupportedMediaType`        |
| 416         | Range Not Satisfiable           | `http.statusRangeNotSatisfiable`         |
| 417         | Expectation Failed              | `http.statusExpectationFailed`           |
| 418         | I'm a teapot                    | `http.statusImATeapot`                   |
| 421         | Misdirected Request             | `http.statusMisdirectedRequest`          |
| 422         | Unprocessable Entity            | `http.statusUnprocessableEntity`         |
| 423         | Locked                          | `http.statusLocked`                      |
| 424         | Failed Dependency               | `http.statusFailedDependency`            |
| 425         | Too Early                       | `http.statusTooEarly`                    |
| 426         | Upgrade Required                | `http.statusUpgradeRequired`             |
| 428         | Precondition Required           | `http.statusPreconditionRequired`        |
| 429         | Too Many Requests               | `http.statusTooManyRequests`             |
| 431         | Request Header Fields Too Large | `http.statusRequestHeaderFieldsTooLarge` |
| 451         | Unavailable For Legal Reasons   | `http.statusUnavailableForLegalReasons`  |
| 500         | Internal Server Error           | `http.statusInternalServerError`         |
| 501         | Not Implemented                 | `http.statusNotImplemented`              |
| 502         | Bad Gateway                     | `http.statusBadGateway`                  |
| 503         | Service Unavailable             | `http.statusServiceUnavailable`          |
| 504         | Gateway Timeout                 | `http.statusGatewayTimeout`              |

If you encounter any issues or would like to contribute to this package, feel free to open an issue or submit a pull request.

### License

This package is open source and available under the MIT License.
