- [0-Bootstrappting steps](#0-bootstrappting-steps)
  - [switching from master branch to step-0](#switching-from-master-branch-to-step-0)
  - [what to do in this step-0 branch](#what-to-do-in-this-step-0-branch)
  - [create a new branch to keep track](#create-a-new-branch-to-keep-track)
  - [`npm install` has update problem](#npm-install-has-update-problem)
  - [`npm start` to see the starting point](#npm-start-to-see-the-starting-point)
  - [What the code is doing?](#what-the-code-is-doing)
  - [Bootstrapping AngularJS Applications](#bootstrapping-angularjs-applications)

# 0-Bootstrappting steps

## switching from master branch to step-0

- `git branch` shows we are at master branch
- `git checkout -f step-0` sent us to *(HEAD detached at step-0) branch*

## what to do in this step-0 branch

- You can look around, make experimental changes and commit them
- you can discard any commits you make in this state without impacting any branches by performing another checkout.

## create a new branch to keep track

- `git checkout -b step-0-bootstrapping-me` to create a new branch
- so that I can save history.md and do other changes
- now `git branch` returns two branches master and the new branch

## `npm install` has update problem

- `karma-chrome-launcher` is outdated
- update `package.json` with the line `"karma-chrome-launcher": "^3.1.x",`
- delete `node_modules` folder and `package-lock.json` and run `npm install` again
- finally the errors are gone

## `npm start` to see the starting point

- `npm start` to start the web server
- if sees the blank webpage with a line of text 'Nothing here yet!', then it works
- we can see the index.html source page [here](./app/index.html)

## What the code is doing?

`ng-app` attribute: `<html ng-app>`

`angular.js`script tag: `<script src='lib/angular/angular.js"></script>`

double-curly binding with an expression: `nothing here {{'yet' + '!'}}`

## Bootstrapping AngularJS Applications

no idea what it is talking about! come back often!!!
