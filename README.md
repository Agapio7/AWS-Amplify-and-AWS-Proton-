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




