# flaskrrr-and-tests
login example for interview only
## QuickStart
No one likes looooong README, so let's begin:
### Version
python 3.9.0  
Flask 1.1.2  
Robot Framework 3.2.2 (Python 3.9.0 on darwin)  
### Preparation
```
git clone https://github.com/NTUEEboy/flaskrrr-and-tests.git
```
Just follow the tutorial of [Flask website](https://flask.palletsprojects.com/en/1.1.x/) to creat a virtual env. under the project
```
$ python -m venv venv
```
Activate the environment and install Flask
```
$ . venv/bin/activate
$ pip install Flask
```
Install [Robot Framework](https://robotframework.org/) for automated UI test
```
$ pip install robotframework
$ pip install --upgrade robotframework-seleniumlibrary
```
Make sure you have your [ChromeDriver](https://chromedriver.chromium.org/) and make it executable
```
$ export PATH=$PATH:path/to/ChromeDriver/
```
### How to run
Start the web server in localhost
```
$ export FLASK_APP=loginApp/main.py
$ flask run
```
The unit test for login system in each cases
```
$ python -m unittest -v loginApp/tests/test_basic.py
```
or if you have pytest installed
```
$ pytest
```
The UI test
```
$ robot loginApp/tests/valid_login.robot
$ robot loginApp/tests/invalid_login.robot
```
