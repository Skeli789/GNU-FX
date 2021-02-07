# ToeFX 
#### Update: Instructions for tests and reports added to the bottom.
A web application that helps patients detect fungal toe infection, and allows them to keep track of their treatment progress.

## Requirements:
* [Nodejs (15.5.1)](https://nodejs.org/en/)
* [Python3](https://www.python.org/downloads/)
* Pillow
* [Tensorflow](https://www.tensorflow.org/install/pip) <br>
Note: Make sure you have python3 alias set as python. Running ```python``` should open an interactive CI.
**A docker file for running server with AI is in the `toefx-server` folder.**
## Instructions:
1. Open a terminal.
2. Navigate to the ```toefx-client``` folder.
3. Install all the required dependencies:<br>
``` Run "npm install" ```
4. Start the front-end server.<br>
``` Run "npm start" ```
5. From the root directory (ToeFX), navigate to the ```toefx-server``` folder.
6. Install all the required dependencies.<br>
```Run "npm install"```
7. Start the back-end server.<br>
```Run "npm start"```
8. Open up a web browser and go to http://localhost:3000/
9. Click ``Login`` at the top of the page. Use the default login username ```demo@example.com``` and the default login password ```123``` to access the application. 

# Tests (unit-test, validation-test, stress and secutirty test)
* Used **Jest** to test the react app and the node app.
* Used **Burp suite professional** for security and stress tests.
* Created a **bot** for validation test (Some part of the validation test is done using Jest but because of security reasons, react/jest does not allow image upload).
## Test reports
* To access the test report generated for the React app, from the root directory, go to `toefx-client` -> `coverage` -> `icov-report` -> `index.html`. 
* To access the test report generated for the Node app, from the root directory, go to `toefx-server` -> `coverage` -> `icov-report` -> `index.html`.
* To access the test report generated by Burp suite, from the root directory, go to `BurpSuite` -> `burp.html` and there is a screen-shot(burp.JPG) showing the number of requests sent.
## How to run the tests
### setup
* Go to `toefx-client` and run `npm install`
* Go to `toefx-server` and run `npm install`
### Run
* To run the **unit tests** for the React app, go to `toefx-client` and run `npm run unitTest`.  The output is  a table showing the percentage of statements coverage, branch coverage, function coverage and line coverage.
* To run the **validation tests** , go to `toefx-client` and run `npm run validationTest`.
* To run the unit-tests for the node app, go to `toefx-server` and run `npm test`. The output is  a table showing the percentage of statements coverage, branch coverage, function coverage and line coverage.
## Instruction to run the bot
* Go to `TestingSelenium` and run `python ./test.py`.
