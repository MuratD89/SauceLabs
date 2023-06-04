# SauceLabs

Below you will find what I use in this project and how I use it. I tried to do the explanations in order according to the file structure in Intellij. 

Base Page:
I initialized the page so I don't keep typing the web driver.
Tests can be run in chrome and firefox.
With the pagemanager initialized method in the base page, we get rid of initializing the pages one by one.
At the bottom, we do the closing process with the tear down method.

Config reader:
I created it to read the inputs in the values

OptionsManager
Here I set the way the pages work. 

Page Manager: 
I made it for initializing the pages.

Config reader option manager and pagemanager I created all of these to help the base page. For example, calling url from config reader method in line 43 in the base page.

Login Page and Home Page
On this page, I used the operations I did in the login section. I also got help from Helpermethod. Here I used the try catch method in case of an error due to the method. If there is an error, try catch will handle it. 
I also added chain method from helpermethot to increase the usability of the code.

Constants:
I connect here from the base page and get the path. I specify here how long it should wait. When I change it from here, it changes everywhere.

HelperMethods
In line 31, I initialized it first so that I can use the methods in order by doing "return this". I used them in pages package.

Javascriptutil 
Javascriptutil is used as helper methods.

Waiting
Here I use the wait method instead of writing the thread as sleep.

Testtoolexception
I created this to use in try catch. If the executing method gives an error, it will find it through this class.
Error codes is a class connected to the test tool exception. It is used for log file.

Hook
Implementing the initialized method in the base page
Taking screen shots before shutting down
And it closes with a tear down.

TestRunner
I used test runner to execute the cucumber tests and manage their execution flow

Stepdefinitions
I wrote my test cases in the following 3 SD files and ran them in cucumber.
- GenericSD
- HomePageSD
- LoginPageSD

Testutil
I have written two methods here for reporting.

Configuration file
This is where we set which browser the test will run on, which url the test will log in to.

Loginpage.feature
Here I wrote my test cases. I also used "scenario outline" which is a nice feature in cucumber. By using this I can do my tests using different users. We can test the same test many times with different users.

Cartoperations.feature
Here I used the data map belonging to cucumber and I used it to give different values over the same test. The difference from Scenario outline is that it runs the test only once.


HTML Report:
After the test runs, go to intellij and open Target package at the bottom and then right click on the cucumber report and click "copy Path/Reference" and select "absolute path". And then open it in Firefox.   

Cucumber report
After the test is finished, scroll down to the bottom of the terminal section, there is a link called cucumber report, if you click directly on it, the report will open.

