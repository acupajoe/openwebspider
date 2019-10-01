# openwebspider(js)

Open Source Web Spider

## Requirements

- MySQL Server / PostgreSQL
- nodejs
- pdftotext (`brew install poppler`)
- `openssl` (to generate a self-signed certificate)

## Install

```sh
$ npm install
$ node src/server.js

# Create Self Signed Certificate
$ cd conf
$ openssl genrsa -out .client-key.pem 2048
$ openssl req -new -key client-key.pem -out client.csr
$ openssl x509 -req -in client.csr -signkey client-key.pem -out client-cert.pem
```

## Getting started

- Open a web-browser at [https://127.0.0.1:9999/](https://127.0.0.1:9999/)
- Go in the third tab (Database) and configure your settings
- Verify that openwebspider correctly connects to your server by clicking the "Verify" button
- "Save" your configuration
- "Create DB"; this will create all tables needed by openwebspider
- (remember that this will remove all existing tables and will create them from scratch)
- Now you are ready to start an openwebspider worker; first tab (Worker): Go

### NOTE

Search and indexer web services holds the connection to the database.
If you change the database settings you should restart the openwebspider's server.

## Web Services

- [Indexer Web Service](http://www.openwebspider.org/documentation/openwebspider-js/openwebspider-indexer-web-service/ "Indexer Web Service")
- [Search Web Service](http://www.openwebspider.org/documentation/openwebspider-js/search-web-service/ "Search Web Service")


## License

The MIT License (MIT)

Copyright (c) 2017 Stefano Alimonti <info@openwebspider.org>

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

http://www.openwebspider.org/license/
