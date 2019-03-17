# AndrewP_REASinatraExercise

# Hello-World Git
git clone https://github.com/Azure-Samples/nodejs-docs-hello-world.git

# Deploy with Kudu builds (Configure a deployment user)
az webapp deployment user set --user-name apaton8410 --password Matrix45#@

# Local Git deployment
az webapp deployment source config-local-git --name <app_name> --resource-group <group_name>

# Enable local Git with Kudu
az webapp deployment source config-local-git --name <app_name> --resource-group <group_name>

# Git-enabled app
az webapp create --name <app_name> --resource-group <group_name> --plan <plan_name> --deployment-local-git

# Az webapp create (JSON)
Local git is configured with url of 'https://apaton8410@<app_name>.scm.azurewebsites.net/<app_name>.git'
{
  "availabilityState": "Normal",
  "clientAffinityEnabled": true,
  "clientCertEnabled": false,
  "cloningInfo": null,
  "containerSize": 0,
  "dailyMemoryTimeQuota": 0,
  "defaultHostName": "<app_name>.azurewebsites.net",
  "deploymentLocalGitUrl": "https://apaton8410@<app_name>.scm.azurewebsites.net/<app_name>.git",
  "enabled": true,
  < JSON data removed for brevity. >
}

# Deploy your project
git remote add azure <url>
git push azure master

# Deploy with Azure DevOps builds
git remote add vsts <url>
git push vsts master
