# React Native - Meteor Boilerplate

A starting point for integrating a React Native app with a Meteor app. I've used this file structure in large, multi-developer projects.

_Note #1:_ This project only specifies an opinion on the *React Native* project architecture.

_Note #2:_ I generally split the React Native app and Meteor app into separate repositories. That's just personal preference. You can keep them in the same repo, as shown here, if you wish.

## Getting started with Meteor

1. Make sure you have [Meteor](https://www.meteor.com/) installed.


## Getting started with React Native

1. Make sure you have [React Native](https://facebook.github.io/react-native/) installed.


## Helpful Commands

From the `RNApp` directory:

- `npm run ios`: Open the app in Xcode and start the packager.
- `npm run android`: Start the app in the android sim?

## Project Organization

Everything discussed in this section pertains to the `RNApp` directory.

First, I've moved nearly all the logic out of `index.ios.js` and `index.android.js` so that we can maximize code reuse. All of our Javascript code will live in the `app/` folder. I'll go through each subfolder below.


### `app/api/`

Any external API calls would live here. I've also considered putting DDP interactions in here as well to clean up the components.

### `app/components/`

These are "dumb" components that make up UI elements. For example: stylized inputs or button components.

### `app/containers/`

These components make up the various "views" of my application. These are things like a sign in screen, settings tab, main tab, etc.

### `app/helpers/`

Basic helpers that I use in various places throughout the app. Sorting, math, etc.

### `app/images/`

Store all your images here. This helps you use a standard approach for images across Android and iOS (a change we saw in React Native version `0.14.0`).

### `app/config.js`

Any configuration for your app. Think of it like a `settings.json` in a Meteor context.

### `app/ddp.js`

My DDP related functions. This file could likely be broken out into its own package but I find myself tweaking it occasionally so I keep it in the project. It's mostly just nice-to-have functions.

### `app/index.js`

The root component of my application. This is where I initialize ddp and is the file that both `index.ios.js` and `index.android.js` require.


## Technologies Used

- [Meteor](https://www.meteor.com/)
- [React Native](https://facebook.github.io/react-native/)
- [Node DDP Client](https://github.com/hharnisc/node-ddp-client) (at version 0.1.1)
- [EJSON](https://github.com/primus/ejson)
- [lodash](https://lodash.com/)
