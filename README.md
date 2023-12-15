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

for workflow from start to end:
from dev branch, create a feature branch or a hotfix branch by doing 'git checkout dev  --> git checkout -b feature/new-code ' &nbsp; &nbsp;
from the feature branch, add your code changes e.g. new lines in terraform or new files
do your code commits e.g. git add . --> git commit -m "message" --> git push 
from your github console, create a new pull request from feature/new-code to dev  , get the approvers' approvals and merge the pull request. this will trigger a deployment in dev
to deploy to uat, from your github console, create a new pull request from dev to uat , get the approvers' approvals and merge the pull request. this will trigger a deployment in uat
to deploy to prod, from your github console, create a new pull request from uat to prod , get the approvers' approvals and merge the pull request. this will trigger a deployment in prod