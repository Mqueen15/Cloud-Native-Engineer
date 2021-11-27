
Creating new endpoints for a Python application by using the Flask framework.
our simple Python application which resides in the `app.py` file.

If we just open that particular file by using the py command, we'll be able to see that we have a Flask application,and then we have a couple of routes 
such as 
* The Main route :

Which is going to return a ''Hello World!'' application


```sh
@app.route("/") 
def hello():
    app.logger.info('Main request successfull')

    return "Hello World!"
```

* Slash Status route :

Return a hard-coded response, which is going to be a JSON response with the main result being ''Okay-healthy'' , and it's going to return a 200 HTTP code, meaning that the request was successful

```sh
@app.route('/status')
def healthcheck():
    response = app.response_class(
            response=json.dumps({"result":"Ok- healthy"}),
            status=200,
            mimetype='application/json'
    )

    app.logger.info('Status request successfull')
    return response
```

* Slash Metrics route :

```sh
@app.route('/metrics')
def metrics():
    response = app.response_class(
            response=json.dumps({"status":"success","code":0,"data":{"UserCount":140,"UserCountActive":23}}),
            status=200,
            mimetype='application/json'
    )

    app.logger.info('Metrics request successfull')
    return response
```

