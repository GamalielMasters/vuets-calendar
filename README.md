# vuets-calendar

A conversion of vuejs-calendar project from vuejsdevelopers/vuejs-calendar to typescript.

## What this is

Continuing with my habit of making my continuning education coursework harder than it needs to be (umm... I mean more interesting and educational), I am taking a similar approach to this project as I did the prior one in this series, namely I'm converting it to TypeScript and vue-class-component.

However, in this case rather than taking the existing project and bolting typescript support onto it, I'm taking a different tact.  I'm generating a skeleton project using vue-cli with Typescript enabled, and them importing the relevent parts from the original skeleton project into this new project.

This repo is the result of that attempt at a franken-baby.

Also, like the prior project in this course, I will be doing the best I can to implement the features before watching the instructor's implementation.  Thus, implementation might well diverge from the established coursework.  I consider this a natural extension of the fact that different developers will naturally implement things differently.

## Why do I do this.

Frankly, I find coursework boring.  Well, let me amend that, learning new things is never boring, but for myself, just watching a course be presented rarely sticks in my long term memory well, and just re-typing / copying the course work into my IDE is mind-numbingly boring, causing my brain to stop functioning and go into copy mode.

One thing I can do to stave this off is to change things up... in some cases (where I'm learning somthing conceptual like development patterns), I'll intentionally do the exercizes in a different language than the instructor is working in, so that I am forced to _think_ through the underlying concepts and translate them into my chosen language.

In other instances, like this where the framework is tied to a particular language, I'll change somthing else for the same reason.  Thus my push to implement in Typescript and with class-components rather then straight vie-js. 

Plus, I'm more likely to write my own projects in Typescript over vanilla Javascript anyway, and this this actually helps me optimize for my likely use-case.

The primary reason for implementing the features before seeing the answer is multi-fold.

1. It keeps me sharp, and again forces me to actually think about how to go about solving problems using the framework rather then just copying someone elses solutions.  This can be nothing but a help when I go to actually use this technology to solve real-world problems where in there are no pre-existing answers.

1. When attempting to solve a problem on my own, I'm forced to read the documentation, and thereby learn things that are not covered in the course, including some things that have been introduced since the course was written.

1. Not only do I learn more when solving the problem on my own, but I get a nice little boost from succeeding that copying the solution presented does not provide.  Plus, I learn more from seeing the presented solution when I've solved it myself and can compare my solution with the instructors.

1. Sometimes I like my solution better.

## How do I use this....

Well, honestly, you don't.  It's just an exercise for my benefit, but if you want to check it out, build it and try it, here's the basics, adapted from the origional course material.

## The original course Vue.js Calendar

Adapted Source code inspired by the [Build A Professional Vue App with Vuex & Server-Side Rendering](https://courses.vuejsdevelopers.com/p/build-vue-vuex-app-ssr?utm_source=github-vjd).

#### Demo

See the original project here: [http://vuejs-calendar.vuejsdevelopers.com/](http://vuejs-calendar.vuejsdevelopers.com/)

__Note:__ this is not a running copy of this project... if you want to see this project in play, you have to clone and build it yourself.

#### Pre-installation

- I built this with the most up-to-date version of node that was available at the time, which was v12.10.0.

- Ensure [Node.js  >=12.10](https://nodejs.org/en/download/), [NPM](https://docs.npmjs.com) and [git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) are installed on your system

#### Installation

1. Install this code on your local system by Cloning the repository on your local file system
    
        ```
        cd /path/to/install/location
        
        git clone https://github.com/GamalielMasters/vuets-calendar.git
        ```  
   
2. Change into directory and do the node dance.

    ```
    cd vuets-calendar
    npm install
    ```

4. [optional] Edit the `.env` file and replace any variables if needed
    
5. Start project

    ```
    npm run serve
    ```

Your site will be available at *localhost:[PORT]* where `PORT` is whatever value is set in your `.env` file.

#### Here are the NPM targets available

#### Project setup
```
npm install
```

##### Compiles and hot-reloads for development
```
npm run serve
```

#### Compiles and minifies for production
```
npm run build
```

#### Run your tests
```
npm run test
```

#### Lints and fixes files
```
npm run lint
```

#### Run your unit tests
```
npm run test:unit
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
