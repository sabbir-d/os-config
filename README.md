# Programming environment for devs

## install vscode
[vscode download link](https://code.visualstudio.com/sha/download?build=stable&os=win32-x64-user)
> customize vscode

[customized jsonc link](https://github.com/sabbir-dcy/os-config/blob/main/vscode-settings.jsonc)

```bash
1. copy full json code from the link above
2. open vscode
3. press ctrl + shift + p
4. search for `open user settings (json)`
5. clear all previous code if there is any.
5. paste to the copied code here and save
```

## vscode extensions

- better comments
- es7+react/redux native snippets
- react extension pack by rajbir
- tailwindcss intellisnense
- markdown all in one
- auto rename tag
- material icon theme
- prettier code formatter
- live server
- live share (optional)

## coding font
- [jetbrains mono](https://download.jetbrains.com/fonts/JetBrainsMono-2.242.zip)

## Install git bash

- download gitbash from [official website](https://github.com/git-for-windows/git/releases/download/v2.38.1.windows.1/Git-2.38.1-64-bit.exe)
- install git bash keeping all the settings to default
- click next next

## Install windows terminal

1. download windows terminal from <a href="https://www.microsoft.com/store/apps/9n0dx20hk701" target="_blank">MS store</a>

> to setup git bash in windows terminal follow the steps below
3. open windows terminal and go to settings
4. add new profile
5. click new empty profile
6. change the name to **gitbash**
7. replace the command line with this location
   `C:\Program Files\Git\bin\bash.exe`
8. choose custom icon or use default icon from this location
   `C:\Program Files\Git\mingw64\share\git\git-for-windows.ico`
9. go startup tab and choose gitbash as default profile

## Install postman
- [postman for desktop](https://dl.pstmn.io/download/latest/win64)


\
 &nbsp;
---

# Python (for windows)

## install vs build tools
- [download vs build tools](https://aka.ms/vs/17/release/vs_BuildTools.exe)
- install `desktop development with c++`
- [reference image](https://github.com/sabbir-dcy/os-config/blob/main/Screenshot%202022-11-21%20223152.png)

## Install python using anaconda distribution

- download conda from [official website](https://repo.anaconda.com/archive/Anaconda3-2022.10-Windows-x86_64.exe)
- click next next untill `advance installation option`
- check both of the options

## Run jupyter notebook on browser

-  open terminal and run the commands below

```sh
jupyter notebook
```
_**this will create notebook file on default browser**_

## Colab local server

> if you are using google colab instead of jupyter notebook you can also use this local compiler for colab

1. copy paste the commands below in terminal
```sh
pip install jupyter_http_over_ws
```

```sh
jupyter notebook --NotebookApp.allow_origin="https://colab.research.google.com" --port=8888 --NotebookApp.port_retries=0
```
2. now the token URL (_local host one_) generated in terminal: [reference image](https://robotwealth.com/wp-content/uploads/2020/11/jupyter-local.png)
3. In Colab, click the `Connect` button and select `Connect to local runtime`. Enter the token URL you just copied and click `Connect`: [reference image](https://robotwealth.com/wp-content/uploads/2020/11/colab-connect-local.png)\
_**Now code will run lot faster**_


\
 &nbsp;
---

# Python (for ubuntu)
## install python & jupyter notebook

1. setting up python - `once`

```sh
sudo apt update
```

```sh
sudo apt install python3-pip python3-dev
```

2. installing python & jupyter - `once`

```sh
sudo -H pip3 install --upgrade pip
```

```sh
sudo -H pip3 install virtualenv
```

3. create a python project directory - `once`
```sh
mkdir ~/python_project
```

4. move inside of that directory - `once`
```sh
cd ~/python_project
```

5. creating virtual environemnt - `once`

```sh
virtualenv python_virtual_env
```

```sh
source python_virtual_env/bin/activate
```

>now your terminal prefix should look similar to this
 `(python_virtual_env) example@host:~/python_project_dir$`

6. installing jupyter - `once`

```sh
pip install jupyter
```

7. running jupyter notebook

```sh
jupyter notebook
```

> below steps are optional who want to use jupyter as a runtime for google colab

8. enable http extension - `once`

```sh
pip install jupyter_http_over_ws
```

```sh
jupyter serverextension enable --py jupyter_http_over_ws
```

9. run jupyter as local runtime
- go to your python environment directory we created earlier
- run command below
```sh
jupyter notebook \
  --NotebookApp.allow_origin='https://colab.research.google.com' \
  --port=8888 \
  --NotebookApp.port_retries=0
```

\
 &nbsp;
---

# React devs
## client packages ||
- [install nodejs](#install-node)
- [create react app](#create-react-app)
- [Tailwind and daisyui](#tailwind)
- [firebase integration](#firebase-integration)
- [authentication](#authentication)
- [react router dom](#react-router-dom)
- [react toastify](#react-toastify)
- [react hot toast](#hot-toast)
- [axios](#axios)
- [react hook form](#react-hook-form)
- [react query](#react-query)
- [Icons](#Icons)
- [react day picker](#react-day-picker)
- [image upload](#image-upload)

## server packages ||

- [express server setup](#express-server)
- [mongodb get started](#mongodb-quick-start)
- [mongoose get started](#mongoose-quick-start)

\
&nbsp;

---

## install node

- [node download link](https://nodejs.org/dist/v18.12.1/node-v18.12.1-x64.msi)

```bash
just agree and click next next
```

## for yarn users install yarn globally

```bash
npm install --global yarn
```

## install nodemon globally for backend

```bash
npm install -g nodemon
#or
yarn global add nodemon
```



## firebase install

```bash
# install firebase tools
npm install -g firebase-tools
```

```bash
firebase login
# press y for giving cli usage access
# after redirect to browser login with google account and give access
```

- `if you face any issue while hosting app on firebase use following commands`

```bash
firebase login --reauth
firebase use --add
```

## heroku install

- [heroku cli download link](https://devcenter.heroku.com/articles/getting-started-with-nodejs#set-up)
- download 64 for windows 10/11 or mac version according to your os
- install the exe file
- click next next
- after installing run the following command on terminal

```bash
heroku login
```

- press any key to open browser
- complete login process

## create react app

```bash
npx create-react-app my-app
#or
yarn create react-app my-app

#create react app with vite
yarn create vite
Project name: » first-react-project
Select a framework: » react
Select a variant: » react
cd first-react-project
yarn
code .
yarn run dev #or for local area network access
yarn run dev --host
```

## [tailwind](https://tailwindcss.com/docs/guides/create-react-app)

## +[Daisy ui](https://daisyui.com/docs/install/)

```bash
yarn add -D tailwindcss postcss autoprefixer
```

```bash
yarn tailwindcss init -p
```

```bash
yarn add daisyui
```

- tailwind.config.js ->

_tip - if you face webpack error while editing config.js file, restart the client_

```js
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ["./src/**/*.{js,jsx,ts,tsx}"],
  theme: {
    extend: {
      // custom theme
      colors: {
        primary: "#0080ff",
      },
    },
  },
  daisyui: {
    themes: false,
    // false means it won't apply daisy ui theme
    // Or
    themes: [],
    // empty array allows you to set background color of html body
  },
  plugins: [require("daisyui")],
};
```

- below code at index.css ->

```css
@import url("https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap");

@tailwind base;
@tailwind components;
@tailwind utilities;

body {
  font-family: "inter", sans-serif;
}
```

\
 &nbsp;

---

## firebase integration

- create firebase/firebase.init.js inside src folder
- copy the code below to that file

```js
import { initializeApp } from "firebase/app";
import { getAuth } from "firebase/auth";

const firebaseConfig = {
  apiKey: process.env.REACT_APP_apiKey,
  authDomain: process.env.REACT_APP_authDomain,
  projectId: process.env.REACT_APP_projectId,
  storageBucket: process.env.REACT_APP_storageBucket,
  messagingSenderId: process.env.REACT_APP_messagingSenderId,
  appId: process.env.REACT_APP_appId,
};

// Initialize Firebase
const app = initializeApp(firebaseConfig);
export const auth = getAuth(app);
```

- create `.env.local` inside root folder of the project
- copy the code bellow and replace `all dummys` with actual key

```
REACT_APP_apiKey=dummyKey
REACT_APP_authDomain=dummyDomain
REACT_APP_projectId=dummyId
REACT_APP_storageBucket=dummyBucket
REACT_APP_messagingSenderId=dummySenderId
REACT_APP_appId=dummy
```

\
 &nbsp;

---

## [authentication](https://github.com/CSFrequency/react-firebase-hooks/tree/master/auth)

### [firebase website](https://firebase.google.com/docs?gclid=EAIaIQobChMIx76hsMfu9wIVydeWCh3F8wpZEAAYASABEgJ_IvD_BwE&gclsrc=aw.ds)

```bash
yarn add firebase
```

```bash
yarn add react-firebase-hooks
```

_tip - don't forget to add providers on firebase website in authentication section before you start coding for the methods._

- ### [sign in with google](https://github.com/CSFrequency/react-firebase-hooks/tree/master/auth#social-login-example)

```js
// sign in with google
import { useSignInWithGoogle } from "react-firebase-hooks/auth";
const [signInWithGoogle, gUser, gLoading, gError] = useSignInWithGoogle(auth);

function handleGoogleSignIn(arg) {
  signInWithGoogle();
}
```

- ### [create user with email](https://github.com/CSFrequency/react-firebase-hooks/tree/master/auth#usecreateuserwithemailandpassword)

```js
// create user with email with email verification
import { useCreateUserWithEmailAndPassword } from "react-firebase-hooks/auth";
const [createUserWithEmailAndPassword, cUser, cLoading, cError] =
  useCreateUserWithEmailAndPassword(auth, { sendEmailVerification: true });

function handleCreateUser(email, password) {
  createUserWithEmailAndPassword(email, password);
}
```

- ### [sign in with email](https://github.com/CSFrequency/react-firebase-hooks/tree/master/auth#usesigninwithemailandpassword)

```js
// login with email and password
import { useSignInWithEmailAndPassword } from "react-firebase-hooks/auth";
const [signInWithEmailAndPassword, eUser, eLoading, eError] =
  useSignInWithEmailAndPassword(auth);

function handleUserSignIn(email, password) {
  signInWithEmailAndPassword(email, password);
}
```

- ### [sign in with github](https://github.com/CSFrequency/react-firebase-hooks/tree/master/auth#social-login-example)

```js
// sigin in with github
import { useSignInWithGithub } from "react-firebase-hooks/auth";
const [signInWithGithub, gitUser, gitLoading, gitError] =
  useSignInWithGithub(auth);

function handleGithubSignIn() {
  signInWithGithub();
}
```

- ### [update profile](https://github.com/CSFrequency/react-firebase-hooks/tree/master/auth#useupdateprofile)

```js
// update user profile
import { useUpdateProfile } from "react-firebase-hooks/auth";
const [updateProfile, updating, updateError] = useUpdateProfile(auth);

async function handleUpdateProfile(arg) {
  await updateProfile({ displayName, photoURL });
  alert("Updated profile");
}
```

- ### [send email verification](https://github.com/CSFrequency/react-firebase-hooks/tree/master/auth#usesendemailverification)

```js
// send email verification
import { useSendEmailVerification } from "react-firebase-hooks/auth";
const [sendEmailVerification, sending, verifyError] =
  useSendEmailVerification(auth);

async function handleSendVerification(arg) {
  await sendEmailVerification();
  alert("Sent email");
}
```

- ### [password reset](https://github.com/CSFrequency/react-firebase-hooks/tree/master/auth#usesendpasswordresetemail)

```js
// password reset email
import { useSendPasswordResetEmail } from "react-firebase-hooks/auth";
const [sendPasswordResetEmail, sending, resetError] =
  useSendPasswordResetEmail(auth);

async function handleResetPassword(arg) {
  await sendPasswordResetEmail(email);
  alert("Sent email");
}

// note: this hook does not give you confirmation if the email is exist or not...it says 'email sent' to any email you geive.ex- yadayada@mail.com

// solution to this you can use firebase default hooks
import { sendPasswordResetEmail } from "firebase/auth";
function handleResetPassword(email) {
  sendPasswordResetEmail(auth, email)
    .then(() => {
      console.log("email sent");
    })
    .catch((error) => {
      console.log(error.message);
    });
}
```

\
&nbsp;

---

## [react router dom](https://reactrouter.com/docs/en/v6/getting-started/tutorial)

```bash
yarn add react-router-dom
```

- ### [react router authentication(require auth)](https://stackblitz.com/github/remix-run/react-router/tree/main/examples/auth?file=src%2FApp.tsx)

```js
// require auth file
import { useAuthState } from "react-firebase-hooks/auth";

function RequireAuth({ children }) {
  const [user, loading] = useAuthState(auth);
  const location = useLocation();

  if (laoding) {
    return <Spinner></Spinner>;
  }
  if (!user) {
    return <Navigate to="/login" state={{ from: location }} replace />;
  }

  return children;
}
export default RequireAuth;
```

```js
// authentication file
const navigate = useNavigate();
const location = useLocation();
const from = location.state?.from?.pathname || "/";

if (user) {
  navigate(from, { replace: true });
}
```

---

- ### [custom active link](https://stackblitz.com/github/remix-run/react-router/tree/main/examples/custom-link?file=src%2FApp.tsx)

```js
function CustomLink({ children, to, ...props }) {
  let resolved = useResolvedPath(to);
  let match = useMatch({ path: resolved.pathname, end: true });

  return (
    <>
      <Link
        style={{ textDecoration: match ? "underline" : "none" }}
        to={to}
        {...props}
      >
        {children}
      </Link>
    </>
  );
}

export default CustomLink;
```

\
&nbsp;

---

## [react toastify](https://fkhadra.github.io/react-toastify/installation)

```bash
# npm
npm install --save react-toastify

# yarn
yarn add react-toastify
```

```js
//inside app.js
import { ToastContainer, Slide } from 'react-toastify'
import 'react-toastify/dist/ReactToastify.css'

fun App() {
  <>
    <ToastContainer autoClose={3000} transition={Slide}/>
    other...compoents
  <>
}
```

```js
// usage
import { toast } from "react-toastify";

toast.success("congrats!");
toast.error("invalid!");
toast.warning("warning");
toast.info("information");
toast("default toast");
```

- ### [see more toast options](https://fkhadra.github.io/react-toastify/introduction)
  \
  &nbsp;

---

## [hot toast](https://react-hot-toast.com/)

```bash
# npm
npm install react-hot-toast
# yarn
yarn add react-hot-toast
```

```js
// inside App.js
import { Toaster } from 'react-hot-toast';

fun App() {

  <div>
    <Toaster position="top-center" toastOptions={{duration: 3000,}}/>
  </div>
}
```

```js
// usage
import toast from "react-hot-toast";
toast.success("Successfully created!");
toast.error("This is an error!");
toast.loading("Waiting...");
toast("Hello World");
```

- ### [see more toast options](https://react-hot-toast.com/)

\
&nbsp;

---

## [axios](https://axios-http.com/docs/example)

```bash
#stable old version
yarn add axios@0.25.0
#or latest version
yarn add axios
```

```js
// axios get method
//----client
useEffect(() => {
  axios("http://localhost:5000/services?name=john", {
    headers: {
      authorization: `bearer secret key`,
    },
  }).then((res) => console.log(res));
}, []);

//-----server
app.get("/services", (req, res) => {
  const authorization = req.headers.authorization;

  const queryParameter = req.query;
  console.log(authorization);
  console.log(queryParameter);
  res.send(services);
});
```

```js
// Axios delete method
//-------client
const handleDelete = () => {
  axios
    .delete(`http://localhost:5000/services/${1}`, {
      // delete method takes body inside data object
      data: {
        service: "body from delete",
      },
      headers: {
        authorization: `bearer secret key from delete`,
      },
    })
    .then((res) => console.log(res));
};

//------------server

app.delete("/services/:id", (req, res) => {
  const query = req.params.id;
  const authorization = req.headers.authorization;
  const service = req.body;
  console.log(authorization);
  console.log(query);
  console.log(service);
});
```

```js
// Axios post method
//--------client
const handlePost = () => {
  axios.post(
    `http://localhost:5000/services`,
    {
      service: "body from post",
    },

    {
      headers: {
        authorization: `bearer secret key from post`,
      },
    }
  );
};

// --------server
app.post("/services", (req, res) => {
  const service = req.body;
  const authorization = req.headers.authorization;
  console.log(service);
  console.log(authorization);
});
```

```js
// axios put method
//------------client
const handlePut = () => {
  axios.put(
    `http://localhost:5000/services`,
    {
      service: "body from put ",
    },
    {
      headers: {
        authorization: `bearer secret key from put`,
      },
    }
  );
};

//-------------server

app.put("/services", (req, res) => {
  const updatedService = req.body;
  const authorization = req.headers.authorization;
  console.log(updatedService);
  console.log(authorization);
});
```

```js
// axios patch method
const handlePatch = () => {
  axios.patch(
    `http://localhost:5000/services`,
    { service: "body from patch" },
    {
      headers: {
        authorization: `bearer secret key from patch`,
      },
    }
  );
};

//-------------server
app.patch("/services", (req, res) => {
  const updatedService = req.body;
  const authorization = req.headers.authorization;
  console.log(updatedService);
  console.log(authorization);
});
```

\
&nbsp;

---

## [axios interceptor]()

```js
import axios from "axios";
import { signOut } from "firebase/auth";
import { auth } from "../firebase/firebase.init";

// create base url
export const axiosPrivate = axios.create({
  baseURL: "http://localhost:5000",
  // baseURL: 'https://example-api.herokuapp.com',
});

axiosPrivate.interceptors.request.use(
  function (config) {
    // attatch authorization access token before sending request
    if (!config.headers.authorization) {
      config.headers.authorization = `Bearer ${localStorage.getItem("token")}`;
    }
    return config;
  },
  function (error) {
    return Promise.reject(error);
  }
);

// Add a response interceptor
axiosPrivate.interceptors.response.use(
  function (response) {
    return response;
  },
  function (error) {
    if (error.response.status === 403 || error.response.status === 401) {
      signOut(auth);
    }
    return Promise.reject(error);
  }
);
```

## use case

```js
// get service by user
// no need to pass auth header as it was inclued through interceptor
useEffect(() => {
  axiosPrivate("/services?name=john").then((res) => console.log(res));
}, []);
```

\
&nbsp;

---

## [react hook form](https://react-hook-form.com/get-started)

```bash
yarn add react-hook-form
```

- ### [sample form](https://react-hook-form.com/get-started#Handleerrors)

- ### [form with basic validation](https://codesandbox.io/s/react-hook-form-basic-validation-qdyye)

\
&nbsp;

---

## [react query](https://react-query.tanstack.com/overview#enough-talk-show-me-some-code-already)

```bash
yarn add react-query
```

```js
// inside index.js
 import { QueryClient, QueryClientProvider, useQuery } from 'react-query'
const queryClient = new QueryClient()
<QueryClientProvider client={queryClient}>
  <App/>
</QueryClientProvider>
```

```js
// usage

//using axios
const { isLoading, error, data, refetch } = useQuery('repoData', () =>
  axios('https://api.github.com/repos/tannerlinsley/react-query').then((res) =>
    console.log(res)
  )
)

if (isLoading) return 'Loading...'

-------------------------------------------------------------------
//using fetch
const { isLoading, error, data,refetch } = useQuery('data', () =>
  fetch('https://api.github.com/repos/tannerlinsley/react-query').then((res) =>
    console.log(res.json())
  )
)
// with dependency
const {isLoading, error, data, refetch } = useQuery(['data', dependency], () => axios('https://api.github.com/repos/tannerlinsley/react-query').then((res) =>
    console.log(res)
  )
)
```

\
&nbsp;

---

## Icons

- ### [react icons](https://react-icons.github.io/react-icons/)

```bash
yarn add react-icons
```

- ### [hero icons](https://heroicons.com/)

```bash
yarn add @heroicons/react
```

- ### [font awesome](https://fontawesome.com/v5/docs/web/use-with/react)

```bash
yarn add @fortawesome/fontawesome-svg-core
yarn add @fortawesome/free-solid-svg-icons
yarn add @fortawesome/react-fontawesome
```

```js
// usage
import { FontAwesomeIcon } from "@fortawesome/react-fontawesome";
import { faCoffee } from "@fortawesome/free-solid-svg-icons";

return (
  <button>
    <FontAwesomeIcon icon={faCoffee} />
  </button>
);
```

\
&nbsp;

---

\
&nbsp;

---

## [react day picker](https://react-day-picker.js.org/start)

```bash
yarn add react-day-picker date-fns
```

```js
import React from "react";
import { DayPicker } from "react-day-picker";

export default function App() {
  // disable all previous days
  const disabledDays = [
    { from: new Date(1600, 0, 1), to: new Date(Date.now() - 86400000) },
  ];

  return (
    <DayPicker
      defaultMonth={new Date()}
      disabled={disabledDays}
      mode="single"
    />
  );
}
```

\
&nbsp;

---

- ### day picker css
  1. create a css file in src folder `daypicker.css`.
  2. import that into App.js `import './daypicker.css' `

```css
.rdp-day_selected:not([disabled]) {
  color: white;
  background-color: #0fcfec;
}

.rdp-day_selected:focus:not([disabled]) {
  background-color: #0fcfec;
  border: 2px solid rgb(138, 238, 252);
}

.rdp-day_selected:hover:not([disabled]) {
  background-color: #19d3ae;
  border: 2px solid rgb(152, 255, 215);
}
.rdp-button:active:not([disabled]) {
  border: 2px solid #19d3ae;
  background-color: #bafff1;
}
```

## image upload

```js
const imageAPI = 'api key from image hosting server'

async function handle() {
  const image = data.image[0]
  const formData = new FormData()
  formData.append('image', image)

  const url = `https://api.imgbb.com/1/upload?key=${imageAPI}`
    // using fetch
    fetch(url, {
      method: 'POST',
      body: formData,
    })

    //or using axios
    axios.post(url, formData ).then....`set hostedUrl to mongodb`
}
```

\
&nbsp;

---

# server

## express server

```bash
# npm
npm init -y
npm install express cors mongodb dotenv jsonwebtoken

# yarn
yarn init -y
yarn add express cors mongodb dotenv jsonwebtoken

# if use yarn you need to add *script* manually to package.json file
  "scripts": {
    "start": "node index.js",
    "start-dev": "nodemon index.js"
  },
```

- ### [express hello world api example](https://expressjs.com/en/starter/hello-world.html)
- ### [dotenv config call](https://github.com/motdotla/dotenv#usage)
- ### [cors usage](https://www.npmjs.com/package/cors#usage)

```js
// sample code
const express = require("express");
const cors = require("cors");
require("dotenv").config();

const app = express();
const port = process.env.PORT || 5000;

app.get("/", (req, res) => {
  res.send("hello world");
});

app.listen(port, () => console.log("listening to port", port));
```

\
&nbsp;

---

## [mongodb quick start](https://www.mongodb.com/docs/drivers/node/current/quick-start/)

- ### [find doc](https://www.mongodb.com/docs/drivers/node/current/usage-examples/findOne/)

- ### [insert doc](https://www.mongodb.com/docs/drivers/node/current/usage-examples/insertOne/)

- ### [delete doc](https://www.mongodb.com/docs/drivers/node/current/usage-examples/deleteOne/)

- ### [update doc](https://www.mongodb.com/docs/drivers/node/current/usage-examples/updateOne/)

- ### [count doc](https://www.mongodb.com/docs/drivers/node/current/usage-examples/count/)

- ### [sort doc](https://www.mongodb.com/docs/drivers/node/current/fundamentals/crud/read-operations/sort/)

- ### [skip and limit doc](https://www.mongodb.com/docs/drivers/node/current/fundamentals/crud/read-operations/limit/#sample-documents)

## mongoose quick start

- install mongodb and mongocompass in your local machine
- then ->

```bash
yarn add express mongoose dotenv cors jsonwebtoken
```

```js
// connecting mongodb through mongoose
const express = require("express");
const mongoose = require("mongoose");
const cors = require("cors");
const routeNameHandler = require("./routeNameHandler.js");
require("dotenv").config();

uri = "mongodbcluster uri";
mongoose
  .connect(uri || "mongodb://localhost/databaseName")
  .then(() => console.log("connection successful"))
  .catch((err) => console.log(err));

const app = express();
const port = process.env.PORT || 5000;
app.use(express.json());

app.use(cors({ origin: "http://localhost:3000" })); // for single route

// or use this for mutiple domain
const whitelist = ["https://example-domain", "http://localhost:3000"];
const corsOptions = {
  origin: function (origin, callback) {
    if (whitelist.indexOf(origin) !== -1) {
      callback(null, true);
    } else {
      callback(new Error("Not allowed by CORS"));
    }
  },
};
app.use(cors(corsOptions));
app.use("/routeName", routeNameHandler);

// global error handler
function errorHandle(err, req, res, next) {
  if (res.headersSent) {
    return next(err);
  }
  res.status(500).json({ error: err });
}

app.listen(5000, () => console.log("listening to the app"));
```

```js
const mongoose = require("mongoose");
const collectionSchema = mongoose.Schema({
  name: {
    type: String,
    required: true,
  },
  email: {
    type: String,
    required: true,
  },
  // restrict input option
  status: {
    type: String,
    enum: ["active", "inactive"],
  },

  // restrict input option + default value
  role: {
    type: String,
    enum: ["user", "admin"],
    default: "user",
  },
});

module.exports = collectionSchema;
```

```js
// application routes

const express = require("express");
const router = express.Router();
const mongoose = require("mongoose");
const collectionSchema = require("./collectionSchema.js");

// create instance of collection schema
const CollectionName = new mongoose.model("CollectionName", collectionSchema);

// get all objects api route
app.get("/", async (req, res) => {
  const query = {};
  const result = await CollectionName.find(query);
  res.json(result);
});

// post api
app.post("/", async (req, res) => {
  const newData = new CollectionName(req.body);
  const result = await newData.save();
  res.json(result, { message: "data posted" });
});

module.exports = router;
```