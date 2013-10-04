# mocksy

Mock http server for testing. Regurgitates the request object.

## Install

```
npm install mocksy --save-dev
```

## Usage

```javascript
var Mocksy = require('mocksy');
var mocksy = new Mocksy({port: 4321});

// In your test runner

describe('Some http endpoint', function () {
  beforeEach(function (done) {
    mocksy.start(done);
  });
  
  afterEach(function (done) {
    mocksy.stop(done);
  });
  
  it('should just work, right?', function (done) {
    // Do your http requests
  });
});

```

## Run Tests

```
npm test
```
