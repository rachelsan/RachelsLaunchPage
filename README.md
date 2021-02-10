# Rachel's Launch Page
A simple launch page with all the neccessary links to do your job.


<img width="1440" alt="rachelslaunchpage" src="https://cloud.githubusercontent.com/assets/1245162/24101064/2ddab1e4-0d4d-11e7-994e-24657fe85f23.png">

## Cloning and deploying this app to IBM Cloud.

By following this guide, you'll be able to fork and clone a copy of this repository and quickly run your own version of the app on IBM Cloud. I've included all the design source files in the design folder in case you want to play with your own robot design and robot animation sequence.

### Prerequisites

You'll need a [IBM Cloud account](https://cloud.ibm.com) and the [IBM Cloud CLI Installer](https://github.com/IBM-Cloud/ibm-cloud-cli-release/releases/) 

### 1. Fork this repository

Click on the fork button located at the top right corner of the view.

<img width="111" alt="screenshot1-fork" src="https://cloud.githubusercontent.com/assets/26547582/24117323/328460ae-0d80-11e7-8b71-8e5fcffd2855.png">

### 2. Clone a copy of the app to your desktop

Click on the Clone or Download dropdown button and select Download to Zip. The source files will be saved to your computer's download folder and will be named RachelsLaunchPage-master. Make sure to rename the folder to the unique name of your app. You'll also need to change the application name in the manifest.yml file.

<img width="443" alt="screenshot2-clonetodesktop" src="https://cloud.githubusercontent.com/assets/26547582/24117339/3d4a5106-0d80-11e7-9909-633a760387cb.png">

### 3. Move the source files to your src folder

Once you've renamed the folder, move it to Documents > src > *yourrenamedfolder*. If you don't have a src folder, I'd recommend creating one. The src folder is a commonly used folder name to organize all project source files.

### 4. Deploy the app

You can use the Cloud Foundry CLI to deploy apps. In the terminal, make sure to change the directory before proceeding.

```
 cd documents
```
```
 cd src
```
```
 cd *youruniqueappname*
```

Set API endpoint to cloud.ibm.com

```
 ibmcloud api cloud.ibm.com
```

You'll be prompted to select from a list. Type 9 for US South.

```
 9
```

Login to your IBM Cloud account using SSO

```
 ibmcloud login --sso
```

Set the target organization and space. Your IBM Cloud ID is your IBM email.

```
 ibmcloud target -c *youribmcloudid* -o *youibmcloudid* -s dev
```

From within the *youruniqueappname* directory push your app to IBM Cloud. 
  
```
 ibmcloud app push
```

This can take a minute. If there is an error in the deployment process you can use the command `cf logs <Your-App-Name> --recent` to troubleshoot. You will need to click on the restart button on the getting started app view to load the app.

<img width="232" alt="screenshot5-restart" src="https://cloud.githubusercontent.com/assets/26547582/24117416/89f11404-0d80-11e7-9400-9f7c2738ab57.png">

View your app at the URL listed in the output of the push command, for example, *myUrl.mybluemix.net*. You can also click on the route url in your Bluemix apps view.

<img width="444" alt="screenshot6-routeurl" src="https://cloud.githubusercontent.com/assets/1245162/24118600/bc644178-0d84-11e7-8616-86e0a682d59e.png">


### 5. Run the app locally

In the terminal enter

```
 npm install
```
```
 npm start
```

View your app at: http://localhost:3000. 
  
If you make changes locally make sure it is synced with your repository on Github. You'll need [Github Desktop](https://desktop.github.com/ "Github Desktop").


