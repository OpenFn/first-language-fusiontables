<<<<<<< HEAD
Language Fusion Tables
==============

Language Pack for building expressions and operations for working with
the [Google Fusion Tables API](https://developers.google.com/fusiontables/).

Documentation
-------------
## Events API

#### Desired `Events API` expression:
```js
events("program", "orgUnit", fields(
  field(...),
  field(...),
  field(...),
  dataValues(
    field("dataElement", "value"),
    field("dataElement", "value"),
    field("dataElement", "value")
  )
))
```

#### Current `Events API` expression—too bulky
```js
event(
  fields(
    field("program", "eBAyeGv0exc"),
    field("orgUnit", "DiszpKrYNg8"),
    field("eventDate", dataValue("date")),
    field("status", "COMPLETED"),
    field("storedBy", "admin"),
    field("coordinate", {
      "latitude": "59.8",
      "longitude": "10.9"
    }),
    field("dataValues", function(state) {
      return [
        { "dataElement": "qrur9Dvnyt5", "value": dataValue("prop_a")(state) },
        { "dataElement": "oZg33kd9taw", "value": dataValue("prop_b")(state) },
        { "dataElement": "msodh3rEMJa", "value": dataValue("prop_c")(state) }
      ]
    })
  )
)
```

## Data Values / Data Value Sets API

#### Desired `DataValueSets API` expression:
```js
dataValueSet("dataSet", "orgUnit", fields(
  field(...),
  field(...),
  field(...),
  dataValues(
    field("dataElement", "value"),
    field("dataElement", "value"),
    field("dataElement", "value")
  )
))
```

#### Current `DataValueSets API` expression—too bulky
```js
dataValueSet(
  fields(
    field("dataSet", "pBOMPrpg1QX"),
    field("orgUnit", "DiszpKrYNg8"),
    field("period", "201401"),
    field("completeData", dataValue("date")),
    field("dataValues", function(state) {
      return [
        { "dataElement": "f7n9E0hX8qk", "value": dataValue("prop_a")(state) },
        { "dataElement": "Ix2HsbDMLea", "value": dataValue("prop_b")(state) },
        { "dataElement": "eY5ehpbEsB7", "value": dataValue("prop_c")(state) }
      ]
    })
  )
)
```

[Docs](docs/index)


Development
-----------

Clone the repo, run `npm install`.

Run tests using `npm run test` or `npm run test:watch`

Build the project using `make`.
=======

# superagent-oauth

A handy [superagent](https://github.com/visionmedia/superagent) plugin to sign requests
with an OAuth token and secret.

Builds on top of [node-oauth](https://github.com/ciaranj/node-oauth), but it enables you
to leverage the API flexibility of superagent instead of the 
`.get`, `.getProtectedResource` and other methods `node-oauth` offers.

## Example

```js
var oauth = new OAuth(…)
  , request = require('superagent');

require('superagent-oauth')(request);

// once you get the access token and secret
request.post('http://api.resource.org/users')
  .sign(oauth, token, secret)
  .send({ my: 'data' })
  .set('X-My', 'Header')
  .end(function (res) {
    console.log(res.status, res.body);
  })
```

## API

### Request#sign

#### OAuth 1.0/1.0a

```js
Request#sign(oauthManager, token, secret)
```

- **oauthManager**: (`OAuth`) instance of the OAuth manager
- **token**: (`String`) access token
- **secret**: (`String`) access token secret

#### OAuth2

```js
Request#sign(oauthManager, token)
```

- **oauthManager**: (`OAuth2`) instance of the OAuth2 manager
- **token**: (`String`) access token

## Credits

(The MIT License)

Copyright (c) 2011 Guillermo Rauch &lt;guillermo@learnboost.com&gt;

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
'Software'), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY
CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
>>>>>>> e4098370437dd2a7cb25230ae386f8a520dcb1b1
