##Flask File Uploads Demo

Here's some code to get you started with file uploads

Some things to remember:

* You must set enctype to multipart/form-data in your form
* You do not need to import any third party libraries.  Flask has everything you need.  Just import os and werkzeug.utils 


You may be wondering about the secure_filename() function.  Or you should be, if you read this code carefully, like we taught you to :)

First, let's understand just a little about what werkzeug does. In our case, Flask builds on top of werkzeug to give you that nice testing server you run everytime you build a Flask app with a server file whose final line is app.run(). Learn more: [http://werkzeug.pocoo.org/](http://werkzeug.pocoo.org/)

Now, why do we need a "secure" file name, and what does that mean, anyway?  All werkzeug is doing for us here is some string parsing, removing any weird special characters like umlauts, or even spaces, things that may cause problems for us when we try to store them and retrieve them from a database.

A couple more points:

* Use the secure filename when you want to store in a database, then retrieve your item from file storage.
* It's fine to store just a few items on your server, or store things temporarily, but try to avoid doing this.  In the future, like during project week, you may want to learn how to store items on remote servers like Amazon's awesome S3 service.
 