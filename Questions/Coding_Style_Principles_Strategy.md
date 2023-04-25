# Coding Style / Principles / Strategy Questions

### **Please Explain What Is TDD (Test Driven Development)?** 
<p align="center">
<img src="img/TDD.png" alt="TDD" title="TDD" width="40%">
</p>

<br/>

> - TDD (Test Driven Development) : An approach to automated software testing that involves writing a failing test before writing the production code to make it pass.
> - Repeat the process below :  <br/>
(1) Add a test 
When performing outside-in TDD, our first step is to create an end-to-end test describing the feature we want users to be able to do.  <br/>
(2) Run all tests. The new test should fail for expected reasons
After we've created our test, the next step in TDD is to run the test and watch it fail. This test will fail (be "red") at first because we haven't yet implemented the functionality. <br/>
(3) Write the simplest code that passes the new test
The next step of TDD is to write only enough production code to fix the current error or test failure. Sometimes we need to step down from the "outside" level of end-to-end tests to an "inside" component test. <br/>
(4) All tests should now pass. <br/>
(5) Refactor as needed, using tests after each refactor to ensure that functionality is preserved.  <br/>

<br/>

### **Why Writing Tests Are Important?**
 > - To test every function and procedure.
 > - To find early bugs and fix in the development cycle and to save costs.
 > - To help the developers to understand the code base and enable them to make changes quickly.
 > - To help for code reuse.

<br/>

### **Explain What Are Functional, Unit, Integration, E2E (End-To-End) Testing?**

> - Functional testing: Testing the functions. 
> - Unit testing: Testing an independent unit of behavior, such as a method (function) in a class.
> - Integration testing: Combines mutiple components testings.
> - End-to-End Testing: Mainly testing the whole working flow,  from the end user’s experience by simulating the real user scenario and validating the system under test and its components for integration and data integrity.

<br/>

### **Explain What Is DDD?** 
> - DDD (Domain Driven Design):  Focus on the core domain and domain logic.
Base complex designs on models of the domain. Constantly collaborate with domain experts, in order to improve the application model and resolve any emerging domain-related issues.

<br/>


# Customized React Questions

### **Why Choose ESLint?**
> - Compared to JSLint, JSHint, ESLint is easy to extend and allow users to customize rules, easy to know where the error is.

<br/>

### **What Are The Important Things You Think About During The Code Review?**
> - Functional programming : focus on high order function and pure function, prevent side effect and mutable data. 
> - Single responsibility : one function only responsible for one functionality. 
> - Open-close : open to extension, close to modification. 
> - DRY principle : Don’t repeat yourself.

<br/>

### **What Does The Clean Code Mean To You?** 
> - Testable, Readable, Maintainable.
