# Welcome to the Readme Page(intended audience is BoomTownROI) .
## I have taken a few notes that may help to build this project on your local host.
Please see dependencies in the [package.json folder](https://github.com/bvjy61u/n/blob/main/package.json)

This program was created with Visual Studio Code.
If you have node.js and npm already installed or you have done this before here are a few steps.

Step 1
On a Windows Environment, open the program "Visual Studio Code". In the top menu 
Terminal>new Terminal>create new folder from the c drive. C:\> mkdir carbajalFolder
Change the directory in terminal to the new folder created and run the following command in the terminal.


npx create-react-app IsraelsNotesApp 

Step 2
Navigate to the folder that is created above from the command line and then run 

npm start 

This should start the local host, if it doesnt install all dependencies or see troubleshooting below. 


Step 3
In the program visual studio code open the folder created.
For example if you created C:\carbajalFolder open this from visual studio code.
There are a few boiler plate files that are not used but you should be able to build the solution or run on local host if you copy paste the code found on github for these files. [Source Code](https://github.com/bvjy61u/n)

App.css <br />
App.js <br />
index.js <br />
main.js <br />
Sidebar.js <br />
package.json <br />



If you would like to redeploy to your own github follow the below instructions (replace with your own urls) 
then run these <br />
	git commit -m "first commit" <br />
	git branch -M main <br />
	git remote add origin https://github.com/bvjy61u/notes.git <br />
	git push -u origin main <br />

npm install --save gh-pages <br />
 
in scripts section of package.json file add these. <br />
 "predeploy": "npm run build", <br />
  "deploy": "gh-pages -d build", <br />
   


///initial commit to github <br />
echo "# notes" >> README.md <br />
git init <br />
git add README.md <br />
git commit -m "first commit" <br />
git branch -M main <br />
git remote add origin https://github.com/bvjy61u/notes.git <br />
git push -u origin main <br />


==============deploy changes(for updates) <br />
git add -A <br />
git commit -m "ChangeCommentOnSubmit" <br />
git push -u origin main <br />

Appendix <br />
further reading :Testing: https://reactjs.org/docs/testing.html <br />

==============Deployment Troubleshooting<br />

Environment Variables check <br />
C:\WINDOWS\System32 <br />
C:\Program Files\nodejs <br />
C:\Program Files\nodejs\node_modules\npm\bin <br />
C:\WINDOWS\System32\WindowsPowerShell\v1.0 <br />
C:\Users{systemname}\AppData\Roaming\npm <br />
=======================npm start fails===============<br />
npm install -g npm@latest <br />
npm start  <br />
npm --version  <br />
npm install -g react-scripts <br />
npm start  <br />
note: run npm start in the same place or folder level as the package.json file <br />
	

1 git init <br />
2 git remote add origin https://github.com/bvjy61u/notes.git <br />
3 git remote set-url origin https://github.com/bvjy61u/notes.git <br />
4 npm run build <br />
5 npm run deploy <br />


==============First update pending <br />
Navigation: To note based on note id. <br />
Input Validation:  Email field, address field, password field, etc <br />
Sample code*: <br />

handleUserInput (e) {
  const name = e.target.name;
  const value = e.target.value;
  this.setState({[name]: value}, 
                () => { this.validateField(name, value) });
}
validateField(fieldName, value) {
  let fieldValidationErrors = this.state.formErrors;
  let emailValid = this.state.emailValid;
  let passwordValid = this.state.passwordValid;

  switch(fieldName) {
    case 'email':
      emailValid = value.match(/^([\w.%+-]+)@([\w-]+\.)+([\w]{2,})$/i);
      fieldValidationErrors.email = emailValid ? '' : ' is invalid';
      break;
    case 'password':
      passwordValid = value.length >= 6;
      fieldValidationErrors.password = passwordValid ? '': ' is too short';
      break;
    default:
      break;
  }
  this.setState({formErrors: fieldValidationErrors,
                  emailValid: emailValid,
                  passwordValid: passwordValid
                }, this.validateForm);
}

validateForm() {
  this.setState({formValid: this.state.emailValid && this.state.passwordValid});
}




Credit is always owed when it is due. <br />
https://www.youtube.com/c/JamesGrimshaw <br />
I created my first react app by watching the above video. <br />
This was my first live deployment to github, sad but true. <br />
I am so gratefule for this coding challenge becuase I have more tools in the toolbox so to speak. <br />
Thank you so Much!<br />




# Below is the standard information populated, when this page was created -  Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

The page will reload when you make changes.\
You may also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can't go back!**

If you aren't satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you're on your own.

You don't have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn't feel obligated to use this feature. However we understand that this tool wouldn't be useful if you couldn't customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Code Splitting

This section has moved here: [https://facebook.github.io/create-react-app/docs/code-splitting](https://facebook.github.io/create-react-app/docs/code-splitting)

### Analyzing the Bundle Size

This section has moved here: [https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size](https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size)

### Making a Progressive Web App

This section has moved here: [https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app](https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app)

### Advanced Configuration

This section has moved here: [https://facebook.github.io/create-react-app/docs/advanced-configuration](https://facebook.github.io/create-react-app/docs/advanced-configuration)

### Deployment

This section has moved here: [https://facebook.github.io/create-react-app/docs/deployment](https://facebook.github.io/create-react-app/docs/deployment)

### `npm run build` fails to minify

This section has moved here: [https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify](https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify)
