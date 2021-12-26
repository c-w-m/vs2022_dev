# [Quickstart: Create your first Python web app using Visual Studio](https://docs.microsoft.com/en-us/visualstudio/ide/quickstart-python?view=vs-2022)

## Notes

### Setup
1. use conda to create python environment
```shell
# activate conda base
$ conda activate base
(base)$ conda create -y --name vs2022_dev39 python=3.9
(base)$ conda activate vs2022_dev39
(vs2022_dev39)$
```
2. vs py package manager did not pip install into the conda environment

### Add code file
3. app.py as directed in tutorial

### Run application
4. set as startup file -> app.py

5. Right-click the project in Solution Explorer and select Properties. Select the Debug tab from the Properties menu, and set the Port Number property to 4449. This setting ensures that Visual Studio launches a browser with localhost:4449 to match the app.run arguments in the code.

6. Select Debug > Start Without Debugging or press Ctrl+F5, which saves changes to files and runs the app.

7. A command window appears with the message Running in https://localhost:4449. A browser window opens to localhost:4449 and displays the message Hello, Python! The GET request also appears in the command window with a status of 200.

If a browser doesn't open automatically, start the browser of your choice and navigate to localhost:4449.

If you see only the Python interactive shell in the command window, or if that window flashes on the screen briefly, make sure app.py is set as the startup file.

8. Navigate to localhost:4449/hello to test that the decorator for the /hello resource also works. Again, the GET request appears in the command window with a status of 200. Try some other URLs as well to see that they show 404 status codes in the command window.

9. Close the command window to stop the app, and then close the browser window.


### Next steps

Congratulations on running your first Python app from Visual Studio. You've learned a little about using Visual Studio as a Python IDE!


Because the steps you followed in this Quickstart are fairly generic, you've probably guessed that they can and should be automated. Such automation is the role of Visual Studio project templates. Go through [Quickstart - Create a Python project using a template](https://docs.microsoft.com/en-us/visualstudio/python/quickstart-02-python-in-visual-studio-project-from-template?view=vs-2022) to create a web app similar to the one in this article, but with fewer steps.

To continue with a fuller tutorial on Python in Visual Studio, including using the interactive window, debugging, data visualization, and working with Git, follow Tutorial: Get started with Python in Visual Studio.

To explore more that Visual Studio has to offer, select the links below.

Learn about [Python web app templates in Visual Studio](https://docs.microsoft.com/en-us/visualstudio/python/python-web-application-project-templates?view=vs-2022).
Learn about [Python debugging](https://docs.microsoft.com/en-us/visualstudio/python/debugging-python-in-visual-studio?view=vs-2022)
Learn more about the Visual Studio IDE in general.

## References

### Framework Comparisons

* [Flask vs Django in 2021: Which Framework to Choose?](https://hackr.io/blog/flask-vs-django)


### Flask

* ["Flask" search on Amazon](https://www.amazon.com/s?k=flask+web+development&gclid=CjwKCAiAn5uOBhADEiwA_pZwcI6YCc3K54qKZ1ud_qFWdiozt96bJ4oIoTOFHMpxazbc8wnpb2Sa1RoCcQQQAvD_BwE&hvadid=241869026526&hvdev=c&hvlocphy=9028882&hvnetw=g&hvqmt=b&hvrand=18041907000765974534&hvtargid=kwd-41435888083&hydadcr=16401_10303663&tag=googhydr-20&ref=pd_sl_66q320mqvv_b)

* [Quickstart: Create your first Python web app using Visual Studio](https://docs.microsoft.com/en-us/visualstudio/ide/quickstart-python?view=vs-2022)
* [Flask Quickstart](https://flask.palletsprojects.com/en/2.0.x/quickstart/#quickstart)
* [Flask: Deployment Options](https://flask.palletsprojects.com/en/2.0.x/deploying/)
* [Flask Quickstart - Rendering Templates (flask.pocoo.org)](https://flask.palletsprojects.com/en/1.0.x/quickstart/#rendering-templates)
* [Tutorial source code on GitHub: Microsoft/python-sample-vs-learning-flask](https://github.com/Microsoft/python-sample-vs-learning-flask)

#### Flask Books and Code Repositories
* [Flask Web Development](https://coddyschool.com/upload/Flask_Web_Development_Developing.pdf), 1ed, 2014
* [Flask Web Development](https://github.com/yogendras843/books/raw/master/Flask%20Web%20Development_%20Developing%20Web%20Applications%20with%20Python%20(%20PDFDrive.com%20).pdf), 2ed, 2018
* [The Flask Mega-Tutorial Part I: Hello, World!](https://blog.miguelgrinberg.com/post/the-flask-mega-tutorial-part-i-hello-world)

* [Mastering Flask Web Development](https://edu.anarcho-copy.org/Programming%20Languages/Python/mastering-flask-web-development-2nd.pdf), 2018

* [Flask Framework Cookbook](https://u1lib.org/dl/5541218/b87eed?dsource=recommend), 2ed 2019
* [code](https://github.com/PacktPublishing/Flask-Framework-Cookbook-Second-Edition)

#### Flask Videos

* [Django vs Flask | Which framework to choose? | Python](https://www.youtube.com/watch?v=MVp80hz4rxM)
* [Learn Flask for Python - Full Tutorial](https://www.youtube.com/watch?v=Z1RJmh_OqeA)
* [The Flask Mega-Tutorial Introduction](https://www.youtube.com/watch?v=9FBDda0NCwo&t=156s)
* []()

### Visual Studio

#### Python projects

* [Python projects](https://docs.microsoft.com/en-us/visualstudio/python/managing-python-projects-in-visual-studio?view=vs-2022)
* [Web project templates](https://docs.microsoft.com/en-us/visualstudio/python/python-web-application-project-templates?view=vs-2022)
* [Django web project template](https://docs.microsoft.com/en-us/visualstudio/python/python-django-web-application-project-template?view=vs-2022)

#### Learn Flask in Visual Studio

* [1 - Create a project and solution](https://docs.microsoft.com/en-us/visualstudio/python/learn-flask-visual-studio-step-01-project-solution?view=vs-2022)
* [2 - Create a Flask app](https://docs.microsoft.com/en-us/visualstudio/python/learn-flask-visual-studio-step-02-create-app?view=vs-2022)
* [3 - Serve static files and add pages](https://docs.microsoft.com/en-us/visualstudio/python/learn-flask-visual-studio-step-03-serve-static-files-add-pages?view=vs-2022)

#### Learn Django in Visual Studio

* [1 - Create a project and solution](https://docs.microsoft.com/en-us/visualstudio/python/learn-django-in-visual-studio-step-01-project-and-solution?view=vs-2022)
* [2 - Create a Django app](https://docs.microsoft.com/en-us/visualstudio/python/learn-django-in-visual-studio-step-02-create-an-app?view=vs-2022)
* [3 - Serve static files and add pages](https://docs.microsoft.com/en-us/visualstudio/python/learn-django-in-visual-studio-step-03-serve-static-files-and-add-pages?view=vs-2022)
* [4 - Use the Django Web Project template](https://docs.microsoft.com/en-us/visualstudio/python/learn-django-in-visual-studio-step-04-full-django-project-template?view=vs-2022)
* [5 - Authenticate users](https://docs.microsoft.com/en-us/visualstudio/python/learn-django-in-visual-studio-step-05-django-authentication?view=vs-2022)

### Azure

2021-10-12
At present, Python is supported on Azure App Service for Linux, and you can publish apps using Git deploy and containers, as described in this article.

* [Publish to Azure App Service](https://docs.microsoft.com/en-us/visualstudio/python/publishing-python-web-applications-to-azure-from-visual-studio?view=vs-2022)
* [App Service on Linux](https://docs.microsoft.com/en-us/azure/app-service/overview#app-service-on-linux)
* [Quickstart: Create a Python app using Azure App Service on Linux](https://docs.microsoft.com/en-us/azure/app-service/quickstart-python?tabs=bash&pivots=python-framework-flask)
* []()



### AWS

* [AWS Elastic Beanstalk](https://aws.amazon.com/elasticbeanstalk/)
* [AWS Elastic Beanstalk Pricing](https://aws.amazon.com/elasticbeanstalk/pricing/)
* [AWS Pricing Calculator](https://calculator.aws/#/)
* [AWS Free Tier](https://aws.amazon.com/free/?all-free-tier.sort-by=item.additionalFields.SortRank&all-free-tier.sort-order=asc&awsf.Free%20Tier%20Types=*all&awsf.Free%20Tier%20Categories=*all)
* []()
