# 100 Days Of Code - Log

### Day 1 June 5, 2017
**Today's project**
MERN Template

**Today's Progress**
  - starting with [hackathon starter](https://github.com/sahat/hackathon-starter) organized the structure of the project to my liking. Added:
    - Structure for React out of the box
    - webpack/ES6
    - Continuous Integration
    - Linting

**Thoughts**
I've been learning a lot of related concepts for full stack JavaScript and wanted to pull all of my learning together into one example. This project will be a jumping off point for the technologies I want to work with while also serving as a reminder on how to get things started.

**Link to work:** 
  - https://github.com/jstoebel/mern_template/commit/ba73a93b8a7d551917f15cc28a7659e5bebd4152
  - https://github.com/jstoebel/mern_template/commit/ba73a93b8a7d551917f15cc28a7659e5bebd4152

### Day 2 June 6, 2017
**Today's project**
MERN Template

**Today's Progress**
  - more formatting and linting changes
  - wireframe for Redux
  - setup for building the server from ES6
**Thoughts**

I think I have a decent set up going! While there is a lot I would like to add, I am ready to move on to my next FCC project. As I make new decisions about changes to structure I will put them back into this repo.

**Link to work:** 
  
 - https://github.com/jstoebel/mern_template/commit/8ed897ed58e295d25cb2c8aecc5db180ca4f81c0
 - https://github.com/jstoebel/mern_template/commit/c94d35759586a4eb300125cd01179d1ee19e3975
 - https://github.com/jstoebel/mern_template/commit/cee7341c5210a5caf75fa611cd75c19518022335
 - https://github.com/jstoebel/mern_template/commit/ef617b372b558125287a10eedff9186088ebd2e9


### Day 3: June 7, 2017
**Today's project**
Nightlife App

**Today's Progress**
  - started on nightlife app
  - implemented controller action to get results fro yelp api

**Thoughts:** 
I'm excited to start a new project with some solid plans!

**Link to work:** 
[https://www.freecodecamp.com/challenges/build-a-nightlife-coordination-app](https://www.freecodecamp.com/challenges/build-a-nightlife-coordination-app)

### Day 4: June 8, 2017

**Today's project**
Nightlife App

**Today's Progress**
  - added script to `package.json` for both development and production envs
  - built redux store
  - enable cache busting by using [html-webpack-plugin](https://medium.com/powerspace-engineering/how-to-cache-busting-with-webpack-5131b4af8826)


**Thoughts** 

With the controller built now its time to starting thinking about how the frontend will function. I want to focus on the first user story but also keep in mind where I will be going in the future. My basic idea for the component structure:

- `App` wraps everything
- contains a `SearchBar`. Submitting to `SearchBar` stores most recent search in store. Results from yelp are also stored kept in store. We'll need to retain this for future user stories
- if results are present in the store display them.
- `Bar` component displays details on single search result

As I built out the store I realized there was some basic set up for the store missing from `src/client.js` I should drop that into my template.

I'm also realizing that cache needs to be busted when rebuilding the client. I'll need to look into this.

**Link to work:** 

https://github.com/jstoebel/nightlife/commit/a08860e35aeb566715ad894ded4a600f2e1be509

### Day 5: June 9, 2017

**Today's project**
JWT/React/Redux authentication (service)

**Today's Progress**
  - implemented login for JWT based auth service based on this tutorial [http://blog.slatepeak.com/refactoring-a-basic-authenticated-api-with-node-express-and-mongo/](http://blog.slatepeak.com/refactoring-a-basic-authenticated-api-with-node-express-and-mongo/)
  - began implementing front end for the same using this tutorial [http://blog.slatepeak.com/build-a-react-redux-app-with-json-web-token-jwt-authentication/](http://blog.slatepeak.com/build-a-react-redux-app-with-json-web-token-jwt-authentication/)

**Thoughts** 

While the Hackathon Starter provides a greater starter for session based authentication it was becoming a pain to not have it be a part of my React single page app. Much as I would have liked to press on with my nightlife app I took the time to understand and implement JWT based authentication. I worked to include this in my MERN template. Once this is done (hopefully tomorrow) I can integrate it into my nightlife app

**Link to work:** 

https://github.com/jstoebel/mern_template/commit/cdfd79681e305b06141090b9c485c1dfa73f8689
https://github.com/jstoebel/mern_template/commit/ef9db09df0e388a7301cf4edeef25e915e56a506

### Day 6: June 10, 2017

**Today's project**
JWT/React/Redux authentication (client)

**Today's Progress**
  - finished a draft of authentication client
  - configure webpack to emit `index.html` links to bundles. This enabled cache busting.

**Thoughts** 

Working through a tutorial I completed a draft of the React/Redux client to handle authentication. I had different ideas on how I wanted to structure things so there was a significant amount of refactoring from the given code. For example, I decided to split components into two parts: the front facing ui and a container the connects action dispatchers and state. This allows for better reusability.

I also ran into some confusion in terms of getting webpack to emit an `index.html` that points to the correct bundle of my client and other assets. The plugin `html-webpack-plugin` was emitting the wrong url for those assets/ After some initial confusion and frustration and figured out how to use `publicPath` to tell webpack how to properly construct the right URL. 

**Link to work:** 

https://github.com/jstoebel/mern_template/commit/5ed8c6cc007ad13447613980fc2942d60c501df9
https://github.com/jstoebel/mern_template/commit/8c8a2e64efc8a77879531a31896eb202b1324679
https://github.com/jstoebel/mern_template/commit/d9146f97fd1b34faebe87b806f0a20be399ab02c

### Day 7: June 11, 2017

**Today's project**
MERN template project

**Today's Progress**
  - ported router to use react-router version 4

**Thoughts** 

The tutorial I am working through uses react-router version 3. There was a big rewrite in version 4 and porting things over is not trivial. Fortunately, this is not a large project and the docs walk you though this change.

I encountered another breaking change with `react-cookie` the tutorial uses version 1, but version 2 is different. Unfortunately in this case, the docs were less clear on how to manage this change.

**Link to work:** 

https://github.com/jstoebel/mern_template/commit/454b891b0cc2c381033efe9a13c454bd6e31da7f

### Day 8: June 12, 2017

**Today's project**
Batavia

**Today's Progress**
  - rough draft of `str.format`

**Thoughts** 

I worked on Batavia last winter and was excited to jump back into it. I created a rudimentary implementation for `.format` along with tests. Advanced features of the method (like alignment, padding, sign handling etc) are not handled yet. My next step will be to create a more robust set of tests and then proceed with TDD to ensure I've covered all of the corner cases.

**Link to work:** 

https://github.com/jstoebel/batavia/commit/deced6862e9ac48d3183b6fed12821159400c200

### Day 9: June 13, 2017

**Today's project**
Batavia

**Today's Progress**
  - more tests for `.format` feature
 
**Thoughts** 

I did more research on this details of `.format`. Namely all of the details listed [here](https://docs.python.org/3/library/string.html#formatstrings). My intention is to approach this problem with test driven development: write the tests first to fully describe the intended behavior and begin to implement. When they all pass I am done. This is going to be a lot of work.

**Link to work:** 
https://github.com/jstoebel/batavia/commit/877c9e1cbd178d0371d9b42494af3df0f07316fd

### Day 10: June 14, 2017

**Today's project**
Batavia

**Today's Progress**
 - change tests to be more specific
  - more work on .format
 
**Thoughts** 

My idea of a single test that attempts every realistic combination of specifier causes a timeout in the CI. Upon further inspection it is a huge over kill. Instead I sat down and wrote out tests trying to cover all of the corner cases

**Link to work:** 
https://github.com/jstoebel/batavia/commit/2df4e7760d7502c04cc53db9de8115590c27b6ac
https://github.com/jstoebel/batavia/commit/4c5c409edd03b34f7f2c0d4e11a3395c2ac4af7d

### Day 11: June 15, 2017

**Today's project**
Batavia

**Today's Progress**
  - more work on `.format`
 
**Thoughts** 

`.format` is a slog but I am make progress. I've done a draft of parsing the specifier. Next up is the functionality to produce the correct substitution.

**Link to work:** 
https://github.com/jstoebel/batavia/commit/2df4e7760d7502c04cc53db9de8115590c27b6ac
https://github.com/jstoebel/batavia/commit/4c5c409edd03b34f7f2c0d4e11a3395c2ac4af7d

### Day 12: June 16, 2017

**Today's project**
Batavia

**Today's Progress**
  - more work on `.format`
 
**Thoughts** 

I finished a partial implementation of `.format` to cover strings. Next up, floats and ints

**Link to work:** 
https://github.com/jstoebel/batavia/commit/9f79d8f668d511c2adf90a22a1db40b307b07061

### Day 13: June 17, 2017

**Today's project**
Batavia

**Today's Progress**
  - more work on `.format`
 
**Thoughts** 

More work on `.format`. Almost done with ints.

**Link to work:** 
https://github.com/jstoebel/batavia/commit/cab0f928e77cdb3a960f9431d1e11081af4a34c6
