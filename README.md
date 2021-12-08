# AWS-Amplify-and-AWS-Proton-

### Overview

* Set of purpose-built architecture and features that provides frontend web and mobile developers to quickly and easily build full-stack applications on AWS.

* Amplify provides two services: 


* Amplify Hosting : a git-based workflow for hosting full-stack serverless web apps with continuous deployment.
* Amplify Studio :  Visual development environment that simplifies the creation of scalable, full-stack web and mobile apps.


## Amplify features


### Hosting Amplify

* It handles the common SPA frameworks, for example, React, Angular, Vue.js, Ionic, and Ember, as well as static site generators like Gatsby, Eleventy, Hugo, VuePress, and Jekyll.

* It manages production and staging environments for your frontend and backend by connecting new branches. 

*	It connects your application to a custom domain, deploy and host SSR web apps created by using the Next.js. framework.

*	It also previews changes during code reviews by setting up pull request previews and improve your app quality with end to end tests. 

*	It protects password on your web app so we can work on new features without making them publicly accessible. 

*	It set up rewrites and redirects to maintain SEO rankings and route traffic as your client app required.

* Its instant cache invalidations assure your app is updated instantly on every code commit.

*	Its atomic deployments remove maintenance windows by ensuring that the web app is updated only after the entire deployment completes. such eliminates conditions where files fail to upload well.

We get screen shots of our app rendered on different mobile devices to identify layout issues.

### Studio

*	In Studio amplify, Visual data modeling helps us to keep attention on our domain-specific objects instead of cloud infrastructure.

* It set up authentication for our app. In addition, it is powerful and easy to understand authorization. Further, its Infrastructure-as-code configures all backend capabilities with AWS CloudFormation.

* It functions with the Amplify Command Line Interface (CLI) where all the updates can be pulled into the CLI. It also invites users through email to log in to the Amplify CLI to configure and manage the backend.

* It has content management with markdown support and manage users and groups for your app. It utilizes studio's visual designer to build frontend UI components from pre-built UI component library.

* It also imports Figma prototypes made by designers into Studio as React code.

*	It also customizes your frontend UI with themes to apply global styles to your app's components. It also configures and test your UI components directly within Studio to view their update and display data.

* Finally, it binds your cloud-connected backend to your frontend UI in a simple way

## AWS Amplify Set Up
* Get log in to the Amplify Console or choose Get Started at the top of the page in AWS Amplify home page.

![image](https://user-images.githubusercontent.com/91752852/145031206-8e6f2360-0f3b-4c3a-82e8-bbb10c3d0922.png)

![image](https://user-images.githubusercontent.com/91752852/145031230-ee3b5521-8037-4519-bd37-6b35b4e690f9.png)

* Once you started from the All apps page, select New app and choose Host web app in the upper right corner of the page.

![image](https://user-images.githubusercontent.com/91752852/145031450-73be9200-8c11-4972-9926-411df61d658f.png)

* Please connect your GitHub, Bitbucket, GitLab, or AWS Code Commit repositories. Alternatively, you can also upload your build artifacts without connecting a Git repository from manual option. Once you authorize the Amplify Console, Amplify fetches an access token from the repository provider, meanwhile, it doesn’t store the token on the AWS servers. Actually, Amplify accesses your repository using deploy keys installed in a specific repository only.

![image](https://user-images.githubusercontent.com/91752852/145031494-630255eb-e239-40c6-8634-9933865872c5.png)

* After that, you can connect the repository service provider, choose a repository, and then choose a corresponding branch to build and deploy.
![image](https://user-images.githubusercontent.com/91752852/145031552-b38ad2ad-c855-4864-acf8-21d2fb75e263.png)

* Confirm build settings for the front end: For the selected branch, Amplify inspects your repository to automatically detect the sequence of build commands to be executed.
![image](https://user-images.githubusercontent.com/91752852/145031612-14fdff51-2ce5-443e-acb3-b797384155d0.png)

* Please verify that the build commands and build output directory i.e artifacts > base Directory is accurate. Choose Edit to open the YML editor to modify the information. Also, you can save your build settings on our servers, or download the YML and add it to the root of your repo (for monorepos, store the YML at the app’s root directory).

* Confirm build settings for the backend: 

 Once you connected a repository provisioned by the Amplify CLI v1.0+ (run amplify -v to find CLI version), the Amplify Console will deploy or automatically update backend resources in a single workflow with the frontend build. You can option to point an existing backend environment to your branch, or create a completely new environment.

![image](https://user-images.githubusercontent.com/91752852/145031689-e99e6e11-eaeb-4e0b-8b51-3c40580bd080.png)

* Create or reuse an AWS Identity and Access Management (IAM) service role to deploy backend functionality using the Amplify CLI during your build, IAM roles are a secure way to grant the Amplify Console permissions to act on resources in your account. Please note that the Amplify CLI won’t run without an IAM service role enabled.

![image](https://user-images.githubusercontent.com/91752852/145031757-008b94e7-c6b3-4bc4-be85-945a06d23dc4.png)

* Save and Deploy: Once you review all of your settings well. Select Save and deploy to deploy your web app to a global content delivery network (CDN). The front end build typically takes few minutes or more based on size of the app.
A build has the following stages:

#### Provision
 
•	Your build environment is set up using a Docker image on a host with 4 vCPU, 7GB memory.
•	 Each build gets its own host instance, ensuring that all resources are securely isolated. 
•	The contents of the Docker file are displayed to ensure that the default image supports your requirements.

#### Build 

* There are three stages: set up, deploy backend and build front end 
* Firstly, it is called setup where it clones repository into container .Secondly runs the Amplify CLI to deploy backend resources) and we lastly build your front-end artifacts.

#### Deploy 
*	Once the build is finish, all artifacts are deployed to a hosting environment managed by Amplify. 
* Every deployment is atomic - atomic deployments removes maintenance windows by ensuring that the web app is only updated after the whole deployment has completed.

#### Verify 
* 	Amplify renders screen shots of the index.html in multiple device resolutions using Headless Chrome to verify that your apps work well.
![image](https://user-images.githubusercontent.com/91752852/145031831-08268bf3-d6f5-481f-a7a1-bc1bd53ee8b0.png)


## Getting started with Amplify Studio

### Get started without your AWS account

*	Without AWS account you can still model and test your data before deploying to the cloud. 
*	After building your data model, you must connect an AWS account to deploy your backend environment to Amplify using Amplify Studio. 
* The sandbox interface lets you perform the following tasks:
* Set up your data model as giveb below.
* Test your new data model locally.
* Deploy your backend to the cloud which requires an AWS account.

### Get started with your AWS account

*	With AWS account you can deploy Amplify Studio to start using all Amplify features, including Data Store, user authentication and authorization, and file storage.
* 	After you deploy a backend in Amplify, you can launch Amplify Studio from your Amplify app. Your whole team can use Studio to add new features, update app data, and manage users and groups.

#### We can get started with a new Amplify app as following steps:

* First Sign in to the AWS Management Console and open AWS Amplify. Choose Create app backend.
* Enter a name for your app and choose Confirm deployment. This deploys a default staging backend environment.
* On the application information page, choose the Backend environments tab.
* Choose Launch Studio. This automatically logs you in to Amplify Studio.
* If you already have an existing backend environment, you can enable Amplify Studio from the console.

In case, you already have an existing backend environment, you can enable Amplify Studio from the console. We can get started from an existing Amplify app as given below.

* First, Sign in to the AWS Management Console and open AWS Amplify. Or, enter amplify console from the Amplify Command Line Interface (CLI).
* In the navigation pane, select Amplify Studio settings.
* Then, turn on Enable Amplify Studio.
* In the Backend environments section, choose Launch Studio. This automatically logs you in to Amplify Studio where you can use all the Studio capabilities.

### Getting started with fullstack continuous deployments

* Please Log in to the Amplify Console and choose Get Started under Deploy. In the below screen, choose From fullstack samples. And you can also start your own adventure by building a backend from scratch by installing the Amplify CLI.

![image](https://user-images.githubusercontent.com/91752852/145033504-b56df110-63b9-4812-87e6-2fb197d144d0.png)


* After that, you have to choose the Authentication Starter and Deploy app. You will be questioned to connect your GitHub account. Connecting your GitHub account permits the Amplify Console to create a fork of the repository in your account, deploy the AWS backend services, and build and deploy the frontend. Further, you will need to create a service role to deploy backend resources to AWS.

![fullstack2](https://user-images.githubusercontent.com/91752852/145033879-0896c329-6c3d-4c02-ab45-e38ad2bc8333.gif)


Explore the fullstack app: 
*	Your app build will begin by deploying the backend followed by the frontend. 
*	Click on the branch name to see the running build. Once the build completes you will be able to see screenshots of your app on different devices.

![image](https://user-images.githubusercontent.com/91752852/145033977-bcf93db2-3054-491a-9dc9-578b6089d24c.png)

At the end of the build, you will have one frontend environment that the main branch deployed at ‘https://main.appid.amplifyapp.com’ and one backend environment named devX. 

*	To add a user to your app, you can either register a user through the deployed frontend, or choose the Authentication tab which links to the Amazon Cognito UserPool. Create a user and try logging in to your app.

![fullstack3](https://user-images.githubusercontent.com/91752852/145034507-faf7b2da-d652-40a6-88bf-5a8f84afec24.gif)

Add a GraphQL backend:	

* Let’s add a GraphQL API backend with a NoSQL database to your app. To start, clone the repository that was forked in your account.

```bash
git clone git@github.com:<username>/create-react-app-auth-amplify.git
cd create-react-app-auth-amplify
```

* From the Backend environments tab, choose Edit backend. As a pre-requisite, follow the information to install and configure the Amplify CLI. The Amplify command line toolchain allows you to edit the backend you just created to add more functionality such as GraphQL/REST APIs, analytics, and storage. Once the Amplify CLI is configured, copy the amplify pull command to connect to this backend from your local machine.

 ```bash
amplify pull --appId XXXXXXXX --envName devw
```
 ![image](https://user-images.githubusercontent.com/91752852/145035153-8388bcdc-19f4-440f-9e0b-f139f740cb13.png)

* Add the GraphQL API using the default to-do example.

```bash
amplify add api
? Please select from one of the below mentioned services GraphQL
? Provide API name: todo
? Choose the default authorization type for the API API key
? Enter a description for the API key:
? After how many days from now the API key should expire (1-365): 7
? Do you want to configure advanced settings for the GraphQL API No, I am done.
? Do you have an annotated GraphQL schema? No
? Do you want a guided schema creation? (Y/n) Y
? What best describes your project: Single object with fields (e.g., “Todo” with ID, name, description)
? Do you want to edit the schema now? No
...
GraphQL schema compiled successfully.
```

* To deploy these changes to the cloud run the following commands.

```bash
amplify push
Current Environment: devw

| Category | Resource name   | Operation | Provider plugin   |
| -------- | --------------- | --------- | ----------------- |
| Api      | todo            | Create    | awscloudformation |
| Auth     | cognitocf0c6096 | No Change | awscloudformation |
? Are you sure you want to continue? (Y/n) Y
..
✔ Generated GraphQL operations successfully and saved at src/graphql
✔ All resources are updated in the cloud
GraphQL endpoint: https://gumwpbojgraj5b547y5d3shurq.appsync-api.us-west-2.amazonaws.com/graphql
GraphQL API KEY: da2-vlthvw5qcffxzl2hibgowv3rdq
```

* Visit the Amplify Console to view the added API category.
* Choosing the API category will allow you to navigate to the AppSync Console to write queries or mutations performing CRUD operations or the DynamoDB Console (to view your Todo table).


![image](https://user-images.githubusercontent.com/91752852/145035516-faf94fc9-0fb1-4737-96f0-5e5a51db4bb5.png)


* Use the Amplify GraphQL client to write frontend code that lists and updates the todos. To deploy the updates to your frontend, simply commit your code and a new build will be triggered in the Amplify Console.


## Building Serverless Web Applications with React & AWS Amplify

Before we started let's visulize ourselves what we have to do to make app
* Firstly, we need a front-end app that we will build using React.js. 
* Secondly, We also want to store the data - DynamoDB with a GraphQL API will manage this for us. 
* Lastly, we want to have an authorization system and we will let AWS Cognito handle it.

![chrome_ftpDvJLmu5](https://user-images.githubusercontent.com/91752852/145196665-5fe173dc-d8a3-4d0a-a142-e752c96e8ad9.png)


###  Step 1 :Prerequisites
*	Before launching app in react you must have installed Node.js v12.x or latest version ,npm v5.x or later and git v2.14.1 or updated version. And also you know well using both JavaScript/ES6 and React.
*	Then you need to have or create AWS account.

#### Install and configure the Amplify CLI
•	The Amplify Command Line Interface (CLI) is a unified toolchain to create AWS cloud services for your app.You can follow one of the given two ways to install the Amplify CLI.

##### Method 1: Installing & Configuring the AWS Amplify CLI Youtube
[![Installing & Configuring the AWS Amplify CLI](https://img.youtube.com/vi/fWbM5DLh25U/0.jpg)](https://www.youtube.com/watch?v=fWbM5DLh25U)

##### Method 2: Follow the instructions below.

##### NPM

```bash
  npm install -g @aws-amplify/cli
```
##### Mac and Linux
```bash
  curl -sL https://aws-amplify.github.io/amplify-cli/install | bash && $SHELL
```
##### Window
```bash
  curl -sL https://aws-amplify.github.io/amplify-cli/install-win -o install.cmd && install.cmd
```

After that Set up the Amplify CLI. Configure Amplify by running the given command:

```bash
amplify configure
```
 * **amplify configure** will ask you to sign into the AWS Console. Then, you're signed in, Amplify CLI will ask you to create an IAM user.
 *  Following this, create a user with **AdministratorAccess** to your account to provision AWS resources for you like AppSync, Cognito etc.

![user-creation](https://user-images.githubusercontent.com/91752852/145173171-f1f7a624-1315-4938-b698-52d9915cacda.gif)

Once the user is created, Amplify CLI will ask you to provide the **accessKeyId** and the **secretAccessKey** to connect Amplify CLI with your newly created IAM user.

```bash
Enter the access key of the newly created user:
? accessKeyId:  # YOUR_ACCESS_KEY_ID
? secretAccessKey:  # YOUR_SECRET_ACCESS_KEY
This would update/create the AWS Profile in your local machine
? Profile Name:  # (default)

Successfully set up the new user.
```
Further, we  will set up the app and initialize Amplify.

### Step 2: Set up fullstack project

#### Create a new React App

* To set up the project, first we'll  create a new React app with create-react-app, a CLI tool used to bootstrap a React app following current best practices. Then, we'll add Amplify and initialize a new project. From your projects directory, run the below commands:

```bash
npx create-react-app react-amplified
cd react-amplified
```

* This creates a new React app in a directory called react-amplified and then moves us into that new directory.Now, we're in the root of the project, we can run the app by using the following command:

```bash
npm start
```

* It runs a development server and allows us to view the output generated by the build, we can see the running app by navigating to http://localhost:3000.

#### Initialize a new backend

* We get running React app, it's time to set up Amplify so that we can create the necessary backend services needed to support the app. From the root of the project, run:
```bash
amplify init
```
•	Once you initialize Amplify you'll be prompted for some information about the app:





```bash
Enter a name for the project (react-amplified)

# All AWS services you provision for your app are grouped into an "environment"
# A common naming convention is dev, staging, and production
Enter a name for the environment (dev)

# Sometimes the CLI will prompt you to edit a file, it will use this editor to open those files.
Choose your default editor

# Amplify supports JavaScript (Web & React Native), iOS, and Android apps
Choose the type of app that you're building (javascript)

What JavaScript framework are you using (react)

Source directory path (src)

Distribution directory path (build)

Build command (npm run build)

Start command (npm start)

# This is the profile you created with the `amplify configure` command in the introduction step.
Do you want to use an AWS profile
```

When you initialize a new Amplify project, you will notice :

* **Amplify**, a top-level directory will be created which stores your backend definition. You'll add capabilities such as a GraphQL API and authentication. Once you add features, the amplify folder will grow with infrastructure-as-code templates create a replicable backend stack.
* **aws-exports.js** will be creates in the src directory that holds all the configuration for the services you create with Amplify. This is how the Amplify client is able to get the necessary information about your backend services.
* **.gitignore** file will be modified  with added some generated files to the ignore list.
* A cloud project is created in the AWS Amplify Console which can be accessed by running **amplify console**. It provides a list of backend environments, deep links to provisioned resources per Amplify category, status of recent deployments, and instructions to promote, clone, pull, and delete backend resources.

#### Install Amplify libraries

* In the beginning, install the necessary dependencies to use Amplify in the client.

```bash
npm install aws-amplify @aws-amplify/ui-react@1.x.x
```
* The aws-amplify package is the main library for working with Amplify in your apps. 
* The @aws-amplify/ui-react package contains React specific UI components used as we build the app.

#### Set up frontend

* Then, we need to configure Amplify on the client to use it to interact with our backend services.
* Once, we open **src/index.js** and add the given code below the last import:

```bash
import Amplify from "aws-amplify";
import awsExports from "./aws-exports";
Amplify.configure(awsExports);
```

* And that's all it takes to configure Amplify. As you add or remove categories and make updates to your backend configuration using the Amplify CLI, the configuration in **aws-exports.js** will update automatically.
* Lastly, our React app is set up and Amplify is initialized. we're ready to add an API in the further step.

### Step 3:Connect API and database to the app

* Currently, you’ve created and configured a React app and initialized a new Amplify project, you can add a feature. The first feature we will add is an API.
* The Amplify CLI prefers creating and interacting with two API known as  REST and GraphQL.
* Here, we will create  GraphQL API using AWS AppSync  and the No SQL database will be Amazon DynamoDB.
Create a GraphQL API and database
* By running the given command from the root of your application directory, a dd a GraphQL API to your app and automatically provision a database.
```bash
amplify add api
```

Accept the default values which are highlighted below:


```bash
? Please select from one of the below mentioned services:
# GraphQL
? Provide API name:
# myapi
? Choose the default authorization type for the API:
# API Key
? Enter a description for the API key:
# demo
? After how many days from now the API key should expire:
# 7 (or your preferred expiration)
? Do you want to configure advanced settings for the GraphQL API:
# No
? Do you have an annotated GraphQL schema?
# No
? Choose a schema template:
# Single object with fields (e.g., “Todo” with ID, name, description)
? Do you want to edit the schema now?
# Yes
```

* The CLI should open this GraphQL schema in your text editor.

**amplify/backend/api/myapi/schema.graphql**


```bash
type Todo @model {
  id: ID!
  name: String!
  description: String
}
```
* The schema generated is for a Todo app. We will notice a directive on the Todo type of @model which is part of the GraphQL transform library of Amplify.
* This Library provides custom directives you can use in your schema .It permits to do things like define data models, set up authentication and authorization rules, configure serverless functions as resolvers, and more.
* A type decorated with the @model directive will scaffold out the database table for the type (Todo table), the schema for CRUD (create, read, update, delete) and list operations, and the GraphQL resolvers needed to make everything work together.
* From the command line, press enter to accept the schema and continue to the next steps.

#### Deploy the API
•	To deploy this backend, run the push command:

```bash
amplify push
```

```bash
? Are you sure you want to continue? Y

# You will be walked through the following questions for GraphQL code generation
? Do you want to generate code for your newly created GraphQL API? Y
? Choose the code generation language target: javascript
? Enter the file name pattern of graphql queries, mutations and subscriptions: src/graphql/**/*.js
? Do you want to generate/update all possible GraphQL operations - queries, mutations and subscriptions? Y
? Enter maximum statement depth [increase from default if your schema is deeply nested]: 2
```

* At this time,the API is live and you can start interacting with it!
* The API once we have deployed is for a Todo app, including operations for creating, reading, updating, deleting, and listing todos.
* Further, run the following command to check Amplify's status:

```bash
amplify status
```
* This will give us the current status of the Amplify project, including the current environment, any categories that have been created, and what state those categories are in. It looks like this;


```bash
Current Environment: dev

| Category | Resource name | Operation | Provider plugin   |
| -------- | ------------- | --------- | ----------------- |
| Api      | myapi         | No Change | awscloudformation |
```

* To view the GraphQL API in the AppSync console at any time, run the following command:

```bash
amplify console api
```


#### Test your API(Optional)

•	To test this out locally, you can run the mock command.

```bash
amplify mock api
```


```bash
# If you have not already deployed you API, you will be walked through the following steps for GraphQL code generation
? Choose the code generation language target: javascript (or preferred target)
? Enter the file name pattern of graphql queries, mutations and subscriptions: src/graphql/**/*.js
? Do you want to generate/update all possible GraphQL operations - queries, mutations and subscriptions: Yes
? Enter maximum statement depth [increase from default if your schema is deeply nested] 2
```

* It will open the GraphiQL explorer on a local port. From the test environment you can try out different operations locally, like queries and mutations.
* You can try running a couple of mutations locally and then querying for the todos:



```bash
mutation createTodo {
  createTodo(input: {
    name: "Build an API"
    description: "Build a serverless API with Amplify and GraphQL"
  }) {
    id
    name
    description
  }
}

query listTodos {
  listTodos {
    items {
      id
      description
      name
    }
  }
}
```

#### Connect frontend to API

* Here, you will create a way to list and create todos from the React application. To do such, you will create a form with a button to create todos and  also way to fetch and render the list of todos.
* Open **src/App.js** and replace it with the following code:



## Deployment

To deploy this project run

```bash
  /* src/App.js */
import React, { useEffect, useState } from 'react'
import Amplify, { API, graphqlOperation } from 'aws-amplify'
import { createTodo } from './graphql/mutations'
import { listTodos } from './graphql/queries'

import awsExports from "./aws-exports";
Amplify.configure(awsExports);

const initialState = { name: '', description: '' }

const App = () => {
  const [formState, setFormState] = useState(initialState)
  const [todos, setTodos] = useState([])

  useEffect(() => {
    fetchTodos()
  }, [])

  function setInput(key, value) {
    setFormState({ ...formState, [key]: value })
  }

  async function fetchTodos() {
    try {
      const todoData = await API.graphql(graphqlOperation(listTodos))
      const todos = todoData.data.listTodos.items
      setTodos(todos)
    } catch (err) { console.log('error fetching todos') }
  }

  async function addTodo() {
    try {
      if (!formState.name || !formState.description) return
      const todo = { ...formState }
      setTodos([...todos, todo])
      setFormState(initialState)
      await API.graphql(graphqlOperation(createTodo, {input: todo}))
    } catch (err) {
      console.log('error creating todo:', err)
    }
  }

  return (
    <div style={styles.container}>
      <h2>Amplify Todos</h2>
      <input
        onChange={event => setInput('name', event.target.value)}
        style={styles.input}
        value={formState.name}
        placeholder="Name"
      />
      <input
        onChange={event => setInput('description', event.target.value)}
        style={styles.input}
        value={formState.description}
        placeholder="Description"
      />
      <button style={styles.button} onClick={addTodo}>Create Todo</button>
      {
        todos.map((todo, index) => (
          <div key={todo.id ? todo.id : index} style={styles.todo}>
            <p style={styles.todoName}>{todo.name}</p>
            <p style={styles.todoDescription}>{todo.description}</p>
          </div>
        ))
      }
    </div>
  )
}

const styles = {
  container: { width: 400, margin: '0 auto', display: 'flex', flexDirection: 'column', justifyContent: 'center', padding: 20 },
  todo: {  marginBottom: 15 },
  input: { border: 'none', backgroundColor: '#ddd', marginBottom: 10, padding: 8, fontSize: 18 },
  todoName: { fontSize: 20, fontWeight: 'bold' },
  todoDescription: { marginBottom: 0 },
  button: { backgroundColor: 'black', color: 'white', outline: 'none', fontSize: 18, padding: '12px 0px' }
}

export default App
```

These are some of the functions:

* **useEffect** : Once the component loads, the **useEffect** hook is called and it invokes the **fetchTodos** function.
* **fetchTodos** : It uses the Amplify API category to call the AppSync GraphQL API with the **listTodos** query. When the data is returned, the items array is passed in to the **setTodos** function to update the local state.
* **addTodo** : It uses the Amplify API category to call the AppSync GraphQL API with the **createTodo** mutation. The major distinguish between the **listTodos** query and the createTodo mutation is that **createTodo** accepts an argument containing the variables needed for the mutation.

## Run locally

* Further, run the app and you should see the form rendered to the screen and be able to create and view the list of todos:

```bash
npm start
```

Well done ! You have successfully deployed your API and connected it with your app.

### Step 4: Add authentication
The next step is  you will be adding  authentication.
Authentication with Amplify

* The Amplify Framework uses Amazon Cognito as the main authentication provider.
* Amazon Cognito is a robust user directory service that handles user registration, authentication, account recovery & other operations.
* Here, you'll learn how to add authentication to your application using Amazon Cognito and username/password login.

#### Create authentication service


```bash
amplify add auth

? Do you want to use the default authentication and security configuration? Default configuration
? How do you want users to be able to sign in? Username
? Do you want to configure advanced settings?  No, I am done.
```

* Run the push command to deploy the service.

```bash
amplify push
```

* Now, the authentication service has been deployed and you can start using it. To view the deployed services in your project at any time, visit to Amplify Console by running the given command:


```bash
amplify console
```



#### Create login UI

* Currently,We have our authentication service deployed to AWS to add authentication to our React app. 
* Creating the login flow might be difficult.  Amplify Framework has an authentication UI component to provide the entire authentication flow for us, using our configuration specified in our **aws-exports.js** file.

* Open src/App.js and make the following changes:

    a.Import the **withAuthenticator** component:

    ```bash
    import { withAuthenticator } from '@aws-amplify/ui-react'
    ```

    b.Change the default export to be the **withAuthenticator** wrapping the main component:
    
    
    ```bash
    export default withAuthenticator(App)
    ```

* Run the app to see the new Authentication flow protecting the app:


```bash
npm start
```

* Now you can see the app load with an authentication flow allowing users to sign up and sign in.
* In this instance, you used the Amplify React UI library and the **withAuthenticator** component to quickly get up and running with a real-world authentication flow.
* You can also tailor this component to add or remove fields, update styling, or other configurations.
* Besides **withAuthenticator**, you can build custom authentication flows using the **Auth** class.
* **Auth** has over 30 methods including **signUp**, **signIn**, **forgotPassword**, and **signOut**.It allow you full control over all aspects of the user authentication flow.  

In the next step, we'll host our app on the Amplify Console, a hosting service complete with a globally available CDN, atomic deployments, easy custom domains, and CI / CD.
 
 ### Step 5: Deploy and host app

* We have made our first app with Amplify. Now, we are going to it to the web with Amplify Console.

#### Add hosting to your app

* You can manually deploy your web app or setup automatic continuous deployment. Here, we'll cover how to manually deploy and host your static web app to quickly share with others. 
* From the root of your project, run the following command and select the **bolded options**.


```bash
amplify add hosting
```


```bash
? Select the plugin module to execute: # Hosting with Amplify Console (Managed hosting with custom domains, Continuous deployment)
? Choose a type: # Manual Deployment
```

#### Publish your app


```bash
amplify publish
```

Finally, Now your app is available online.

![image](https://user-images.githubusercontent.com/91752852/145192301-b6e5fdf7-dbfb-4485-b1e3-1c0392b380b2.png)



* Once you published, your terminal will display your app URL hosted on a **amplifyapp.com** domain. When you make extra changes to publish, just re-run the **amplify publish** command.
* You may get an "AccessDenied" error if your app's distribution directory is not set well. To fix this, please change the distribution directory via **amplify configure project** and then re-run **amplify publish**.
* To view your app and hosting configuration in the Amplify Console, run the **amplify console** command.

Run **amplify delete** command to delete all the environments of the project from the cloud and wipe out all the local files created by Amplify CLI. Now, to see changes, run **amplify status** command.
