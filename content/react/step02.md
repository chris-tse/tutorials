{{#template name="react-step02"}}

In order to take advantage of our database and manipulate our data in more powerful ways we need to create a _collection_, which is where we will store our _documents_ or objects.

> You can read more about collections [here](http://guide.meteor.com/collections.html).

In this step we will implement all the necessary code to have a basic collection for our tasks up and running using React hooks.

## Step 2.1: Create Tasks Collection

We can create a new tasks collection by creating a module at `imports/api/tasks.js` which instantiates a new Mongo collection and exports it.

{{> DiffBox tutorialName="simple-todos-react" step="2.1"}}

Notice that we stored the file in the `imports/api` directory, which is a sensible place to store API-related code, like publications and methods.

> You can read more about app structure [here](http://guide.meteor.com/structure.html).

## Step 2.2: Initialize Tasks Collection

For our collection to work we need to import it in the server so it sets some plumbing up. You can either use `import "/imports/api/tasks"` or `import tasks from "/imports/api/tasks"` if you are going to use on the same file, but make sure it is imported.

Now it is easy to check if there is data or not in our collection, otherwise we can insert some sample data easily as well.

{{> DiffBox tutorialName="simple-todos-react" step="2.2"}}

## Step 2.3: Render Tasks Collection

Now comes the fun part, we will render our tasks using a React Functional Component and a Hook called `useTracker` from a package called [react-meteor-data](https://atmospherejs.com/meteor/react-meteor-data). Every time the data changes through reactivity our component will re-render.

> For more information about React Hooks click [here](https://reactjs.org/docs/hooks-faq.html).

{{> DiffBox tutorialName="simple-todos-react" step="2.3"}}

{{/template}}