This is a simply Web Application for REST API program using Python and Flask\

1) -Before you run this web application, you need to install the packages that are required for the application to run. On the terminal, run the following command to install the packages.\

2) python3 -m pip install flask --if using visual code terminal\

3) Once the flask package is installed, run server.py to start a server which is listening at port 5000 and serving a REST API endpoint at the root / that returns the string Hello World!. Example ip is http://127.0.0.1:5000 \  

4) The reason why using port 5000 is due to the python file we did't not specify the port , When no port is specified, starts at default port 5000\

Example Command and output have used in the terminal of visual studio code:\
theia@theia-ngzhenghuinz:/home/project$ touch /home/project/server.py\
theia@theia-ngzhenghuinz:/home/project$ python3 -m pip install flask\
Defaulting to user installation because normal site-packages is not writeable\
Collecting flask\
  Downloading flask-3.0.3-py3-none-any.whl (101 kB)\
     ━━━━━━━━━━━━━━━━━━ 101.7/101.7 KB 3.8 MB/s eta 0:00:00\
Collecting blinker>=1.6.2\
  Downloading blinker-1.8.2-py3-none-any.whl (9.5 kB)\
Collecting itsdangerous>=2.1.2\
  Downloading itsdangerous-2.2.0-py3-none-any.whl (16 kB)\
Collecting Jinja2>=3.1.2\
  Downloading jinja2-3.1.4-py3-none-any.whl (133 kB)\
     ━━━━━━━━━━━━━━━━━ 133.3/133.3 KB 16.4 MB/s eta 0:00:00\
Collecting Werkzeug>=3.0.0\
  Downloading werkzeug-3.0.3-py3-none-any.whl (227 kB)\
     ━━━━━━━━━━━━━━━━━ 227.3/227.3 KB 29.7 MB/s eta 0:00:00\
Collecting click>=8.1.3\
  Downloading click-8.1.7-py3-none-any.whl (97 kB)\
     ━━━━━━━━━━━━━━━━━━━ 97.9/97.9 KB 16.0 MB/s eta 0:00:00\
Collecting MarkupSafe>=2.0\
  Downloading MarkupSafe-2.1.5-cp310-cp310-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (25 kB)\
Installing collected packages: MarkupSafe, itsdangerous, click, blinker, Werkzeug, Jinja2, flask\
Successfully installed Jinja2-3.1.4 MarkupSafe-2.1.5 Werkzeug-3.0.3 blinker-1.8.2 click-8.1.7 flask-3.0.3 itsdangerous-2.2.0\
theia@theia-ngzhenghuinz:/home/project$ python3 server.py\
 * Serving Flask app 'My Hello World Application'\
 * Debug mode: on\
WARNING: This is a development server. Do not use it in a production deployment. Use a production WSGI server instead.\
   * Running on http://127.0.0.1:5000\
Press CTRL+C to quit\
 * Restarting with stat\
 * Debugger is active!\
 * Debugger PIN: 120-993-187\
127.0.0.1 - - [06/Jul/2024 00:59:18] "GET / HTTP/1.1" 200 -\
127.0.0.1 - - [06/Jul/2024 00:59:25] "GET / HTTP/1.1" 200 -\
127.0.0.1 - - [06/Jul/2024 00:59:26] "GET /favicon.ico HTTP/1.1" 404 -\
