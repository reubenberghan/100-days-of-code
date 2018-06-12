# #100DaysOfCode Log - Round 1 - Reuben Berghan

The log of my #100DaysOfCode challenge. Started on May 26, Saturday, 2018.

## Log

### R1D1 
Been working on my **JavaScript development environment** project to create a starter kit for JavaScript projects. I needed to have a quick way to be able to write modern JavaScript (so transpile with Babel) that had both dev and prod build pipelines with linting and testing baked in. The dev build needed to re-run the build including linting and tests for each files and the prod build should minify the code and handle browser caching by hashing the files.

Today I added a couple of packages, modified the webpack config to add source mapping and the html webpack plugin as well as adding an open:src script to abstract the transpiling of the src code and spinning up of the dev server to a separate script from the start.

### R1D2
Today I continued working on the **JS dev env** project.

I was able to:
- incorporate htmlwebpackplugin into the webpack build which dynamically build the index.html file with the correct asset bundles (e.g. <script/> and stylesheet tags)
- added linting via eslint to the project

### R1D3
Continued with the **JS dev env** project. Today I looked into testing frameworks specifically Jest and how this would fit into my project and was able to add the testing scripts and packages for Jest into the JS dev env project.

### R1D4
Today I added a script to log a message to the console as a prestart script to the **JS dev env** project. I also added an example module with test.

### R1D5
Today in the **JS dev env** project I decided to replace thhe Jest test framework with Mocha in order to have the flexibility and because I felt more comfortable with the style of Mocha. I also modularised some more of the example code.

### R1D6
Continued working on the **JS dev env** project adding a few config items to the project covering:
- node version in package.josn
- nvm config file
- travis ci config file
- editor config file

I also added CI to the repo and a bit code cleanup.

### R1D7
Today I moved on to HTTP call support in the **JS dev env** project using the whatwg-fetch package to be deployed as part of any app built. Though this is a supported browser api it will still be required for some older browsers. I also added some example hardcoded data to be served from the dev server for testing purposes.

### R1D8
Today I continued working on the api support int the example app for the **JS dev env** project. I updated the app to render the returned json data in html if the call was successful.

### R1D9
Today I worked on adding a mock api server and schema to the **JS dev env** project. This was done using the json-server and json-schema-faker packages and adding a mock schema and scripts to spin up an in memory mock mapi server that generates random data each time it is spun up.

### R1D10
Continued with the **JS dev env** project today and set up localtunnel which allows the development project to be shared from my local machine externally while in development.

### R1D11
Today I forked the 100-days-of-code repo so that I could complete my log. Also attended a local meetup for JavaScript juniors focused around React and Redux. The plan is split into groups to work together on a project using React and Redux.

### R1D12
After having issues with adding the hash to the css files during the build in my **JavaScript dev env** I decided to create a new project and work through the intro guide examples to get a better understanding of the webpack features and whether the hashing would work following their examples.

I did not quite get to the Caching guide which covers the hashing of output filenames for caching purposes but got familiar with some other new features particularly the webpack-dev-server package for spinning up a dev server to run the dev build. This works in a very similar way to combining the Express, webpack-dev-middleware, and Open packages. The differences being that the latest webpack and webpack-dev-server incorporate HMR pushing code up to the client as files are saved without the need for a browser refresh. The webpack-dev-middleware option does allow the developer more control / configuration over the dev server though.

### R1D13
Able to continue with the webpack guides and have found a couple of things as part of the **JS dev env** project.

First still unsure about how the Tree Shaking feature works as the follwoing the examples I was unable to see this in action. Also unsure where the definition of marking files as side-effect-free is required, the guides mention the package.json but it is not explicit whether this is my projects packag.json or the 3rd party libraries...

### R1D14
Continued with the webpack guides and was able to get the prod build to add the hash to the extracted css files.

Also integrated the webpack-dev-server and webpack-cli into my **js-dev-env** project replacing the need for manageing a separate srcServer.js file and build.js file while still getting the same benefits. Using the webpack-dev-server has also allowed me to leverage the HMR benefits of webpack in my dev build.

Tomorrow I will need to look at the prod deploy steps and plan my next project, a meal plan with shopping list app. I will be able to use my js-dev-env as a starting point for the tooling and build chain and react for the front end library. Firstly I will need to test out how integrating react and the necessary packages into my dev env.
