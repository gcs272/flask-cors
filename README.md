# Flask-CORS

Flask-CORS is a simple extension to Flask allowing you to support
cross origin resource sharing (CORS) using a simple decorator.

[![Build Status](https://travis-ci.org/wcdolphin/flask-cors.png?branch=master)](https://travis-ci.org/wcdolphin/flask-cors)

## Installation

Install the extension with using pip, or easy_install.
```bash
$ pip install flask-cors
```

## Usage
This extension exposes a simple decorator to decorate flask routes with. Simply
add `@cross_origin()` below a call to Flask's `@app.route(..)` incanation to
accept the default options and allow CORS on a given route.


### Simple Usage

```python
@app.route("/")
@cross_origin() # allow all origins all methods.
def helloWorld():
  return "Hello, cross-origin-world!"
```

### Using defaults
Alternatively, setting your application's `CORS_ORIGINS` configuration property
will

```python
app.config['CORS_ORIGINS'] = ['Foo', 'Bar']
@app.route("/")
@cross_origin() # will return CORS headers for origins 'Foo' and 'Bar'
def helloWorld():
  return "Hello, cross-origin-world!"
```


For a full list of options, please see the full [documentation](http://flask-cors.readthedocs.org/en/latest/)


## Tests
A simple set of tests is included in `test.py`. To run, install nose, and simply invoke `nosetests` or run `python test.py` to exercise the tests. 

## Contributing
Questions, comments or improvements? Please create an issue on [Github](https://github.com/wcdolphin/flask-cors), tweet at [@wcdolphin](https://twitter.com/wcdolphin) or send me an email.


[![Bitdeli Badge](https://d2weczhvl823v0.cloudfront.net/wcdolphin/flask-cors/trend.png)](https://bitdeli.com/free "Bitdeli Badge")

