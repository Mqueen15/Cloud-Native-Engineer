
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

* Slash Status route (endpoint) :

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

* Slash Metrics route (endpoint):

Hardcode a JSON response. Where we return the status being successful, that can return a code zero which means the requests has been successful. Then we can have metrics for the user account or the amount of user which are active. 

We return at 200, which ensures that the request was successful

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

To run this application, we're going to use a Python command. Make sure that Python already has been installed on your machine !

We have an application running on localhost on port 5000. This port is the default port which is going to be opened by the Flask web server.

![N|Solid](https://github.com/Mqueen15/Cloud-Native-Engineer/blob/main/SUSE%20Linux%20Enterprise%20servers,/Architecture%20Consideration%20for%20Cloud%20Native%20Applications/localhost%20&%20port.png?raw=true)

If we go to localhost, which is going to be on 127.0.0.1 on port 5000 and click "Enter", then we'll see our main ''Hello World!'' message, which we expect from our application

![N|Solid](https://github.com/Mqueen15/Cloud-Native-Engineer/blob/main/SUSE%20Linux%20Enterprise%20servers,/Architecture%20Consideration%20for%20Cloud%20Native%20Applications/main%20route.png?raw=true)

We've created two new endpoints a status and the metrics. 


If we navigate back to our bar and after the port 5,000 we input a forward slash status, we'll be able to see our hardcoded result with, ''Okay-healthy''
![N|Solid](https://github.com/Mqueen15/Cloud-Native-Engineer/blob/main/SUSE%20Linux%20Enterprise%20servers,/Architecture%20Consideration%20for%20Cloud%20Native%20Applications/status%20endpoint.png?raw=true)



