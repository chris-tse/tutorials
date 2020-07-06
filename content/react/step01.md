{{#template name="react-step01"}}

In this tutorial we will build a simple to-do tasks app using [React](https://reactjs.org) with the Meteor platform. Meteor works out-of-the-box with several other frameworks like [Blaze](https://guide.meteor.com/blaze.html), [Angular](https://guide.meteor.com/angular.html) and [Vue](https://guide.meteor.com/vue.html). 

## Step 1.1: Create Meteor Project

First we need to install Meteor and the easiest way to setup Meteor with React is by using the command:

```
meteor create --react simple-todos-react
```

After this command is run, Meteor will create several boilerplate files for you.

These are the files responsible for bootstrapping your client user interface:

For now you don't need to worry about the files located in the `client` directory, Meteor has already set them up for you.

You can run your Meteor app using: 

```
meteor run
```

Don't worry, Meteor will keep your app in sync with all your changes from now on.

Most of your React application will be located inside the `imports` directory, and this file is the entry point of your React To-do app:


> Note: in previous versions of Meteor, the `imports` directory was special because files outside the `imports` directory were loaded automatically when the application started, whereas files inside the `imports` directory were only loaded when imported using an `import` declaration or a `require` statement. As of Meteor 1.7, the entry point for both client and server JavaScript is determined by the `meteor.mainModule` section in `package.json`. In other words, as far as JavaScript code is concerned, the entire application now behaves as if it was inside an `imports` directory, so you don't need to worry as much about the `imports` directory now.


## Step 1.2: Create Task Component

After we have all the files set, we can create our first React component for our To-Do App.

{{> DiffBox tutorialName="simple-todos-react" step="1.2"}}


## Step 1.3: Create Sample Tasks

Let's define some sample data which will be used shortly.

{{> DiffBox tutorialName="simple-todos-react" step="1.3"}}

## Step 1.4: Render Sample Tasks

Now we can implement some simple rendering logic with React. We can now use our previous `Task` component to render our list items.

{{> DiffBox tutorialName="simple-todos-react" step="1.4"}}

{{/template}}