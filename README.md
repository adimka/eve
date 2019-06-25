# Project EVE
[![Known Vulnerabilities](https://snyk.io/test/github/connexta/eve/badge.svg?targetFile=package.json)](https://snyk.io/test/github/connexta/eve?targetFile=package.json)

The new wallboard project

## Build
```
yarn build
yarn start
```

## Setting up Slack
Using Slack on the wallboard relies on setting the ```SLACK_TOKEN``` and ```SLACK_CHANNEL```
environment variables. Assign ```SLACK_TOKEN``` to the token for the workspace. Assign ```SLACK_CHANNEL```
to the channel ID of the channel you want to connect to.
  
Set both of these variables before running ```yarn start```.
  
*Windows:* You can set env variables by using the command ```setx -m <Var_Name> <Var_Value```  
Note that the ```-m``` flag makes it a system property so the command line shell must be run in 
administrator mode.  
Example: ```setx -m SLACK_TOKEN 12345```
  
*UNIX:* You can set env variables by using the command ```export <Var_Name>=<Var_Value>```  
Example: ```export SLACK_TOKEN=12345```

## Format Code
Use `prettier` for code formatting through yarn:  
```
yarn prettier --write <file>
```  
  
Prettier can also be used through extensions in your IDE.   
More information can be found [here](https://prettier.io/).  
  
## Docker
On linux run ```make image``` to generate the image.  
  
To push, run ```make push```
  
To run the image, run ```docker run -d -e SLACK_TOKEN=<token> -e SLACK_CHANNEL=<channel> -p 3000:3000 <image-id>```
  
Once the image is running, you can connect to the wallboard app by going to ```0.0.0.0:3000``` in your web browser.
