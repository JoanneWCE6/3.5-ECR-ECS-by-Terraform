**STEP 1**-  After log into AWS Console, under ECR page, click on 'Create repository' under public registry. In the Create public repository page, change repo name with joannew/simple-node-app.

**STEP 2**- Click into the Repo and look for 'View push commands' butoon (top right side). 

**STEP 3**- Open Visual Studio code and Run the Given Commands One By One:

-> aws ecr-public get-login-password --region us-east-1 | docker login --username AWS --password-stdin public.ecr.aws/u2q1a2y8

-> docker build -t joannew/simple-node-app .

-> docker tag joannew/simple-node-app:latest public.ecr.aws/u2q1a2y8/joannew/simple-node-app:latest

-> docker push public.ecr.aws/u2q1a2y8/joannew/simple-node-app:latest

**STEP 4**- Go back to AWS console and click into my own repo, the 'latest' image tag will be showing in the repo.

