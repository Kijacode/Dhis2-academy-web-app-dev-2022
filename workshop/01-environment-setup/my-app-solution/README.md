## CodeSandbox TEST instructions

Once you get to the sign in page, you will need to enter the following:

server: https://debug.dhis2.org/academy
username: admin
password: district

If everything works, you should see a Welcome page on the right side of your CodeSandbox project.

## Can't connect to the server?

Check this link for some troubleshooting tips:
https://github.com/dhis2/academy-web-app-dev-2022/blob/main/resources/DEBUG.md


## To edit/test this project

- In order to edit this project to see if everything works, you will need to sign in using your GitHub account
- Then, fork the project
- To test, you can change something in the `App.js` file (try changing the text in the `h1` tag, save the file and see if the changes are reflected in the browser)

For more information on how to use CodeSandbox, please check this document:
https://github.com/dhis2/academy-web-app-dev-2022/blob/main/resources/CODESANDBOX.md


## Available Scripts

In the project directory, you can run:

### `yarn start`

Runs the app in the development mode.<br />
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.<br />
You will also see any lint errors in the console.

### `yarn test`

Launches the test runner and runs all available tests found in `/src`.<br />

See the section about [running tests](https://platform.dhis2.nu/#/scripts/test) for more information.

### `yarn build`

Builds the app for production to the `build` folder.<br />
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.<br />
A deployable `.zip` file can be found in `build/bundle`!

See the section about [building](https://platform.dhis2.nu/#/scripts/build) for more information.

### `yarn deploy`

Deploys the built app in the `build` folder to a running DHIS2 instance.<br />
This command will prompt you to enter a server URL as well as the username and password of a DHIS2 user with the App Management authority.<br/>
You must run `yarn build` before running `yarn deploy`.<br />

See the section about [deploying](https://platform.dhis2.nu/#/scripts/deploy) for more information.

## Learn More

You can learn more about the platform in the [DHIS2 Application Platform Documentation](https://platform.dhis2.nu/).

You can learn more about the runtime in the [DHIS2 Application Runtime Documentation](https://runtime.dhis2.nu/).

To learn React, check out the [React documentation](https://reactjs.org/).
