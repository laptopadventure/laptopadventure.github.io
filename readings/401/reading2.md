# Reading 2

[Back to the table of contents](../../README.md)

## An introduction to NodeJS and Express

- Explain middleware, answer as though I were a non-technical recruiter.
  - Middleware is the in-between code between two services. So frontend talks to backend, the middleware would be the code that handles the requests the frontend is making.
- Express the most popular \_\_ ** \_\_**.
  - Express is the most popular Node web framework.
- Express is “unopinionated.” What does that mean?
  - For context, opinionated and unopinionated mean they care a specific "right way" to do a task or not. Express isn't, so it doesn't care.
- What is a module and why is modularity useful to us as developers?
  - Modules are packages of code others wrote that you can import andd use in your project, and they can save you a ton of time doing tasks the greater code community has "already solved", in essence.

## What is NPM?

- What version of npm are you running on your machine?
  - 8.12.1
- What command would you type to install a library/package called ‘jshint’ into your node project?
  - `npm install jshint`

## What is TDD?

- Explain why tests are important. Please explain as though I were your non technical elder.
  - Tests are important because as a project grows, developers cannot account for every single niche interaction between all the systems in an application. One change on one side of the application may unintentionally effect another side, and testing manually can only be so vigorous. So automated tests are implemented to do some of the work for us, asserting that things have not broken.
- What are three expected benefits of testing
  - Teams report less defect rates (unintentional problems from code, however that appears)
  - Those same teams report that the overhead of adding the automated testing is far less than the saved effort in making sure everything works
  - Though unproven, practitioners of testing generally say testing leads to higher code standards and quality. Whether or not that is tangential (coder is already a good coder, so they add tests) or not the effect is reported
- Name at lest 2 individual pitfalls and at least 2 team pitfalls commonly encountered while writing tests.
  - Individual Pitfalls
    - forgetting to run tests enough, when they can be automated. For manual testing people might be waiving that to save time too, especially in applications that must compile, if that takes a decent amount of time.
    - writing tests that have the wrong scope, aka too large of a test or too croarse-grained on one thing.
  - Team Pitfalls
    - Partially adopted aka some members on the team didn't implement testing and so their work doesn't get tested/tests implemented for it
    - Poor maintenance of the test suites that, over time, end up with them being overly long and trouble to run often.

## CI/CD

- What are three benefits of Continuous Integration?
  - Catches bugs
  - Reduce amount of merge conflicts
  - Ensure that everyone's changes get integrated
- What is the difference between Continuous Delivery and Continuous Deployment?
  - Continuous Delivery is about developing software in a way where you COULD release it at any time.
  - Continuous Deployment is for automatic deployment right into production as soon as it is ready, because you follow CD
- Explain how GitHub fits into this process assuming the listener comes from a non-technical background
  - GitHub uses a system that sends little messages whenever you do development related things like adding new code to the project. These messages can go anywhere, like another server for automatically running and testing the code. After that, it will send something back to GitHub so GitHub can tell you how the testing went.
