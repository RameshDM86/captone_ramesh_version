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

