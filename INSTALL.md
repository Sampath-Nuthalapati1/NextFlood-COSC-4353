## NextFlood

#### Login

Email: unit-test@gmail.com

Password: 123456

## Prerequisites

1. [Install Visual Studio](https://visualstudio.microsoft.com/downloads/)
2. [Install Visual Studio Code](https://code.visualstudio.com/download)
3. [Install NodeJS](https://nodejs.org/en/download/)
4. [Install MySQL Workbench](https://dev.mysql.com/downloads/workbench/)
5. [Install Git](https://git-scm.com/downloads)


## Steps to clone the repository

1. Open Git Bash.
2. Change the current working directory to the location where you want the cloned directory.
3. Type `git clone`, and then paste the following URL https://github.com/Sampath-Nuthalapati1/NextFlood-COSC-4353.git.
4. Press Enter to create your local clone.
5. Once the repository is cloned to your local computer, open the location of the cloned repositry.

## Setting up the UI

1. Go to the /UI directory and then do `npm install`
2. To setup the Firebase authentication, follow this [link](https://blog.logrocket.com/user-authentication-firebase-react-apps/)
3. Do the necessary code changes and once the application is ready to be hosted, install [Amplify CLI](https://docs.amplify.aws/cli/start/install/)
4. To deploy the web application to AWS using amplify CLI, follow this [link](https://aws.amazon.com/blogs/aws/host-your-apps-with-aws-amplify-console-from-the-aws-amplify-cli/).

## Setting up the DB

1. Create and Connect to a MySQL Database with [Amazon RDS](https://aws.amazon.com/getting-started/hands-on/create-mysql-db/)
2. Create the Database Scheme using the Scripts which are avaialable at ([DB/README.md](https://github.com/Sampath-Nuthalapati1/NextFlood-COSC-4353/blob/main/DB/README.md)

##### Note

Change the connection string in the appsettings.json file in the API solution with the above created MySQL Database

## Setting up the API

1. Go to the./API/ folder in your local computer.
2. Open the NextfloodAPI.sln
3. Build the solution using `dotnet build` to make sure the Web API is working properly.
4. To deploy the Web API on AWS, we first need to run the following command run `dotnet publish -c release`
5. Then zip the contents present at /bin/Release/netcoreapp3.1/publish as NextfloodAPI.zip
6. Now upload the above zipped folder into AWS Lambda using the instructions given in the [link](https://docs.aws.amazon.com/lambda/latest/dg/gettingstarted-package.html)

