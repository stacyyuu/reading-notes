## Express, NPM, TDD, CI/CD

### An intro to NodeJS and Express

1. Explain middleware, answer as though I were a non-technical recruiter.
- Middleware functions typically perform some operation on the request or response and then call the next function in the 'stack', which might be more middleware or a route handler. The order in which middleware is called is up to the app developer. 
- Middleware refers to any behind the scenes software that allows the operating system and the application to communicate and interact with each other. 
- It also helps separate process, applications, and software components to exchange info either within the same device, or between multiple devices. 
- You can compare middleware to a translator helping people who speak different languages understand each other. 

2. Express the most popular __ __ ____.
- The most popular Node web framework and is the underlying library for a number of other popular Node web frameworks. 
- It provides mechanisms to:
- Write handlers for requests with different HTTP verbs at different URL paths (routes).
- Integrate with 'view' rendering engines in order to generate responses by inserting data into templates. 
- Set common web application settings like the port to use for connecting and the location of templates that are used for rendering the response. 
- Add additional request processing 'middleware' at any point within the request handling pipeline. 

3. Express is “unopinionated.” What does that mean?
- Web frameworks often refer to themselves as 'opinionated' or 'unopinionated'. 
- Opinionated frameworks are those with opinions about the 'right way' to handle any particular task. They often support rapid development in a particular domain (solving problems of a particular types) because the right way to do anything is usually well-understood and well-documented. 
- Unopinionated frameworks have far fewer restrictions on the best way to glue components together to achieve a goal, or even what components should be used. They make it easier for developers to use the most suitable tools to complete a particular task, at the cost you need to find those components yourself. 
- Express is unopinionated. You can insert almost any compatible middleware you like into the request handling chain, in almost any order you like. You can structure the app in one file or multiple files, and using any directory structure. 

4. What is a module and why is modularity useful to us as developers?
- A module is a JS library/file that you can import into other code using Node's require() function. 
- This allows you to break up your code in separate files and makes it easier to maintain. 

### NPM
- npm is the world's largest software registry. It is used to share and borrow packages. It consists of three components:
- Website, command line interface(CLI), and registry. 
- npm is installed with Node.js. It stands for Node Package Manager. 
- All npm packages are defined in package.json. 

1. What version of npm are you running on your machine?
- 8.19.3

2. What command would you type to install a library/package called ‘jshint’ into your node project?
- npm install jshint

### TDD
- Test-driven development comes in three phases: coding, testing (in the form of writing unit tests), and design (in the form of refactoring).
- Test cases are developed to specify and validate what the code will do. 
- The simple concept is to write and correct the failed tests before writing new code (before development). This helps to avoid the duplication of code as we write a small amount of code at a time in order to pass tests. 

1. Explain why tests are important. Please explain as though I were your non technical elder.
- Fewer bugs and errors are the primary benefit of TDD. When the code has fewer bugs, you'll spend less time fixing them than other programming methodologies. 
- It produces a higher overall test coverage and therefore a better quality of the final project. 

2. What are three expected benefits of testing
- Reductions in defect rates
- Developers naturally produce cleaner, more readable, and manageable code with TDD
- Developers narrow their focus to a single feature at a time, not moving onto the next until the associated unit test passed

3. Name at lest 2 individual pitfalls and at least 2 team pitfalls commonly encountered while writing tests.
- Individual: forgetting to run tests frequently, writing too many tests at once, or writing tests that are too large. 
- Team: use TDD inconsistently, fail to maintain suites of tests, leading to overly long run times, or abandoning TDD test suites due to overly long run times or team turnover. 

### CI/CD

- Continuous Integration: Each change submitted to an app, even to dev branches, is built and tested automatically and continuously. These tests ensure the changes pass all tests, guidelines, and code compliance standards you established for your app. 

1. What are three benefits of Continuous Integration?
- Makes software development easier, faster, and less risky for developers. 
- By automating builds and tests, developers can make smaller changes and commit them with confidence. 
- Developers get feedback on their code sooner, increasing the overall pace of innovation. 

2. What is the difference between Continuous Delivery and Continuous Deployment?
- Continuous Delivery: extension of continuous integration since it automatically deploys all code changes to a testing and/or production environment after the build stage.
- This means that on top of automated testing, you have an automated release process and you can deploy your app any time by clicking a button. 
- Continuous Deployment: Goes one step futher than continuous delivery. With this practice, every change that passes all stages of your production pipeline is released to your customers. 
- There's no human intervention and only failed test will prevent a new change to be deployed to production. 
- An excellent way to accelerate the feedback loop with your customers and take pressure off the team as there isn't a 'release day' anymore. 
- Developers can focus on building software and they see their work go live minutes after they've finished working on it. 

3. Explain how GitHub fits into this process assuming the listener comes from a non-technical background
- Developers are able to work on a single project in different branches. Once changes have been made, they are able to merge the branches to one with it being compared to the main in order to make sure the changes are not conflicting. You are also able to view all of the commits made to the repo. 