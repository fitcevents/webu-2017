An Introduction to the World of Testing for Front-End Developers
---------------------------------------------
*with [Haris Mahmood](http://www.meetharis.com/)*

#What exists in the world of front-end testing and how to use these tools

##Why test?
- faster to automate than manually
- tests can serve as documentation of the app, helping other devs understand what the app is intended
- easier to find and test edge cases
- more reliable
- prevent major errors that could destroy your business

##Linting
- run through terminal or plugins for your IDE
- provide inline suggestions about improving code formatting
- you can define your company's style guides for code and ensure everyone conforms
- ESLint has become the defacto linter over the past few years
- Airbnb's code styles are one of the most popular starting point

##Test Frameworks
- Testing structure, often using BDD approach
- organize your test by component, features and sub-features
- ie. Calculator has add, subtract, etc. Within add you might test that 1+1=2

Assertions are functions that ensure you get back the results you expect
Jasmine, Chai, most frameworks have similar approaches using assertions, and just vary the syntax for writing your tests.

Spy - lets you monitor a function and ensure that it's running the number of times you expect it to run. Can be used on 
callbacks as well to check when, if and how often the callback was run. 

Stubs - let you create or replace the results of a function. Commonly used for API requests, or features that 
haven't been developed yet. An API stub will return the expected data for your tests to us without actually requiring access 
to the API.

Generate and display the results of your tests.

##Different Kinds of Tests

Unit Tests - you pass in an input and test that you get the expected results. Use code coverage tools to ensure all your 
functions are covered.

Integration Tests - test that a set of functions return the expect results and that they work together.

Functional Tests - tests that check particular user scenarios work as expected.

Snapshot Tests - take a snapshot of the app in one state, compare to the initial snapshot and ensure that they are the same.

##Test frameworks
[Jasmine](https://jasmine.github.io/) - has everything you could need to do all your testing right out of the box. It's very popular in the Angular world.   
[Karma](https://karma-runner.github.io/1.0/index.html) - test runner  
[Mocha](https://mochajs.org/) - requires plugins to handle assertions, spies, etc. Requires more setup up front, but very modular.  
[Jest](https://facebook.github.io/jest/) - built by Facebook as a wrapper around Jasmin, adding a number of features, made it easier to get started and improved 
it's performance. Jest is often used with React.  

##Other Tools
[Istanbul[(https://github.com/gotwarlost/istanbul) - code coverage  
[Enzyme](https://github.com/airbnb/enzyme) - assertion lib for React  
[Sinon](http://sinonjs.org/) - provides spies, stubs and mocks  
others - need to get from Haris' slides!  

##Where to start
- recommends starting with [Jest](https://facebook.github.io/jest/)  
- maybe you switch to something else eventually, but super fast to get going with Jest  

###Q&A
How much time do you spend writing test?  
About 50% of dev time is in the tests. Might write 100 lines of test code for a 5 line function.  

I
