
Creating new endpoints for a Python application by using the Flask framework.
our simple Python application which resides in the 'app.py' file.

If we just open that particular file by using the py command, we'll be able to see that we have a Flask application,and then we have a couple of routes 
such as 
*Main route
which is going to return a ''Hello World!'' application
```sh
@app.route("/") 
def hello():
    app.logger.info('Main request successfull')

    return "Hello World!"
```

