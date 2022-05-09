# Initial Environment Setup

This task will help you get familiar with the DHIS2 CLI. You will also learn how to initialize a new DHIS2 application and you will follow these same steps before you start building your [Project](../../projects/project/README.md)

## Pre-requisites

1. Install [Node.js](https://nodejs.org/en/download/)
2. Install [Yarn 1](https://classic.yarnpkg.com/en/docs/install)

## Install the DHIS2 CLI

```sh
yarn global add @dhis2/cli
d2 help
```

## Initialize a new DHIS2 app

**Note:** Before you initialize your app, please make sure that you do the following:

1. [Create a branch](https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/creating-and-deleting-branches-within-your-repository#creating-a-branch) in your repository for this task and name it 👉 `01-setup-environment`
> Make sure that you're working on this branch. For more details, please check the [get started](../../resources/GET_STARTED.md#how-to-submit-assignments) guide on working and submitting assignments

2. Check that you're in the correct working directory:

On your terminal, navigate to the directory where you'll be working:

```
cd workshop
cd 01-environment-setup
```

Now that you're in the `01-environment-setup` directory, you're ready to create a new DHIS2 app! ✨

### Create `my-app`

We'll use the [d2-app-scripts init command](https://platform.dhis2.nu/#/scripts/init) to **create a new DHIS2 app**:

```sh
d2 app scripts init my-app
cd my-app
ls
```

> **NOTE** If you call `d2 app scripts init my-app`, a new directory will be created at `./my-app` with a pre-populated `package.json`.  You can also run `d2 app scripts init .` to upgrade an existing app in the current directory.

**OR, if you don't have `d2` installed globally**

```sh
npx @dhis2/cli-app-scripts init my-app
cd my-app
ls
```

Once you've created `my-app`, your directory structure should look like this:

```
 ── workshop
    ├── 00-introduction
    ├── 01-environment-setup
    │   ├── README.md
    │   ├── my-app
    │   └── my-app-solution
```

## Set up code-style with DHIS2 style

D2-style[d2-style](https://cli-style.dhis2.nu/) is a tool that runs [`prettier`](https://prettier.io/) and [`eslint`](https://eslint.org) under the hood with [a standardized configuration](https://github.com/dhis2/cli-style/tree/master/config/js).  It also installs git hooks with [husky](https://github.com/typicode/husky) which will automatically check your code style before making a `git` commit!

Following the DHIS2 styleguide isn't strictly required, but it can be very helpful in ensuring you write clean, readable, and functional code for your DHIS2 apps!

```sh
yarn add @dhis2/cli-style --dev
yarn d2-style add eslint react
yarn d2-style install
```

This will set up the project to automatically follow the DHIS2 style guidelines

## Add lint and format scripts

Then, add the following scripts to `package.json`:

```js
// package.json
{
    // ...
    "scripts": {
        // ...
        "lint": "yarn d2-style check",
        "lint:staged": "yarn lint --staged",
        "format": "yarn d2-style apply",
        "format:staged": "yarn format --staged"
    }
}
```

And try out your new scripts!

```sh
yarn lint
yarn format
```
## Start your DHIS2 application locally

Please follow [these steps](../../resources/GET_STARTED.md#start-your-dhis2-application-locally) to start your application on your browser.

## Submit your assignment

When you're ready, please follow these [instructions](../../resources/GET_STARTED.md#how-to-submit-assignments) for submitting your assignment.
