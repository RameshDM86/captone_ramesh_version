# captone_ramesh_version
-
Our Team 1 webpage for a new start-up using HTML5 Dimensions template : https://html5up.net/dimension with CICD pipelines so that future changes can be incorporated efficiently.

**Webpage is currently static webpage.** 

The workflow/Architecture is as the digram below:
 
<img width="467" alt="only_with_snyk" src="https://github.com/RameshDM86/captone_ramesh_version/assets/137069406/8f4fcdca-10af-46e5-a3be-0aaa20432985">

Architecture
-	Simple S3 bucket set up in 3 environments
-	Dev 
-	UAT
-	 Prod
-	Each environment has its own tf files. 
-	S3 bucket set to public so the webpage is currently viewable by the public in all 3 environments.

<br> for workflow from start to end:</br> 
<br> from dev branch, create a feature branch as feature test br by doing `git checkout dev  --> git checkout -b feature/feature test br ` &nbsp; &nbsp;
from the feature branch, add our code changes or amendment e.g. new lines in terraform or new files </br>
<br> Perform code commit for example as `git add . --> git commit -m "Testing branching approval" --> git push` &nbsp; &nbsp; </br>

![github code ](https://github.com/RameshDM86/captone_ramesh_version/assets/137069406/a5212b47-f951-4459-800d-23a4d9e408b5)

![open for pull requests and require approval by approving party](https://github.com/RameshDM86/captone_ramesh_version/assets/137069406/7dcc53d1-80d7-4764-ab7b-d6ed4728c06b)




<br>from github console, create a new pull request from `feature/new-code` to `dev`  , get the approvers' approvals and merge the pull request. this will trigger a deployment in `dev` </br>
<br> to deploy to uat, from your github console, create a new pull request from `dev` to `uat` , get the approvers' approvals and merge the pull request. this will trigger a deployment in `uat` </br> 
<br> to deploy to prod, from your github console, create a new pull request from `uat` to `prod` , get the approvers' approvals and merge the pull request. this will trigger a deployment in `prod` </br>
