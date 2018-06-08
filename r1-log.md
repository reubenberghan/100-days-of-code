# #100DaysOfCode Log - Round 1 - Reuben Berghan

The log of my #100DaysOfCode challenge. Started on May 26, Saturday, 2018.

## Log

### R1D1 
Been working on my JavaScript development environment project to create a starter kit for JavaScript projects. I needed to have a quick way to be able to write modern JavaScript (so transpile with Babel) that had both dev and prod build pipelines with linting and testing baked in. The dev build needed to re-run the build including linting and tests for each files and the prod build should minify the code and handle browser caching by hashing the files.

Today I added a couple of packages, modified the webpack config to add source mapping and the html webpack plugin as well as adding an open:src script to abstract the transpiling of the src code and spinning up of the dev server to a separate script from the start.

### R1D3

### R1D4

### R1D5

### R1D6

### R1D7

### R1D8

### R1D9

### R1D10

### R1D11
Today I forked the 100-days-of-code repo so that I could complete my log. Also attended a local meetup for JavaScript juniors focused around React and Redux. The plan is split into groups to work together on a project using React and Redux.

### R1D12
After having issues with adding the hash to the css files during the build in my JavaScript dev env I decided to create a new project and work through the intro guide examples to get a better understanding of the webpack features and whether the hashing would work following their examples.

I did not quite get to the Caching guide which covers the hashing of output filenames for caching purposes but got familiar with some other new features particularly the webpack-dev-server package for spinning up a dev server to run the dev build. This works in a very similar way to combining the Express, webpack-dev-middleware, and Open packages. The differences being that the latest webpack and webpack-dev-server incorporate HMR pushing code up to the client as files are saved without the need for a browser refresh. The webpack-dev-middleware option does allow the developer more control / configuration over the dev server though.

### R1D13
Able to continue with the webpack guides and have found a couple of things.

First still unsure about how the Tree Shaking feature works as the follwoing the examples I was unable to see this in action. Also unsure where the definition of marking files as side-effect-free is required, the guides mention the package.json but it is not explicit whether this is my projects packag.json or the 3rd party libraries...
