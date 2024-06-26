## Readme Information
> [!NOTE]
> **I started from the official Flask Documentation https://flask.palletsprojects.com/en/3.0.x/**
> 
Until further notice this is exactly, what you can find in here. 
The idea is to further from there later on. But the Documentation is basically from the flask documentation site!

## How to install it?
1. Go into a Command line folder, where you clone this git.
2. Clone this git via:
```sh
git clone git@github.com:ManuelEitel/flask-my-practice-blog.git
```
3. Initialize the Database in the root folder of the cloned git.
```sh
flask --app flaskr init-db
```
4. Run this app in the root folder of the cloned git.
```sh
flask --app flaskr run
```
5. Open a browser of your choice on your computer and open the website.
- http://127.0.0.1:5000/auth/login

You shoud see the main page:
![Main Page](Readme_pngs/main_page.png)

## Installation
Go into your folder of the cloned git.
```sh
pip install -e .
```
Check with
```sh
pip list
```
You should see something like this:
```
Package        Version   Location
-------------- --------- ----------------------------------
click          6.7
Flask          1.0
flaskr         1.0.0     /home/user/Projects/flask-tutorial
itsdangerous   0.24
Jinja2         2.10
MarkupSafe     1.0
pip            9.0.3
Werkzeug       0.14.1
```
## Testing
You should install into your virtual environment these packages
```sh
pip install pytest coverage
```
Then you can test via the command:
```sh
pytest
```
And should see:
```
========================= test session starts ==========================
platform linux -- Python 3.6.4, pytest-3.5.0, py-1.5.3, pluggy-0.6.0
rootdir: /home/user/Projects/flask-tutorial
collected 23 items

tests/test_auth.py ........                                      [ 34%]
tests/test_blog.py ............                                  [ 86%]
tests/test_db.py ..                                              [ 95%]
tests/test_factory.py ..                                         [100%]

====================== 24 passed in 0.64 seconds =======================
```
Or you can type
```sh
coverage run -m pytest
```
and get a coverage report via
```sh
coverage report
```
which will look like this:
```

Name                 Stmts   Miss Branch BrPart  Cover
------------------------------------------------------
flaskr/__init__.py      21      0      2      0   100%
flaskr/auth.py          54      0     22      0   100%
flaskr/blog.py          54      0     16      0   100%
flaskr/db.py            24      0      4      0   100%
------------------------------------------------------
TOTAL                  153      0     44      0   100%
```
or even go via browser
```sh
coverage html
```
and go to your browser and get the site
htmlcov/index.html
