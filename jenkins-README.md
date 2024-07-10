Q: what is jenkins and ci/cd process?

ans: jenkins ci cd to tool by using which i would be able to manage the entire continous intigration continous deployment  from the creation of pull request to the deployment continous delivering our newly created images in the dev and qa images and we would be using muitilple pliugin inorder to achive this like git SCM pluging and maven and sonarqube plugins.

Q: what kind of plugins you have written in jenkins?

ans: i have worked on multiple pipeline and diclarative pipeline  and scripted pipelines 

Q: explain the declarative pipeline syntax used in jenkins?

ans: declarative pipeline would be following particular syntax where these pipelines would be starting of with pipeline inside which i would be having stages and inside the stages would be stage and inside stage would be have steps.
i would be having multiple stage inside the stages such that i would be able to configure these and would be able wirite parllel as well in order to pallel execute multiple stages at a single time. 

Q: explain the master slave architecture?

ans: by using a master slave architecture i wiould be able to reduce the load on the master by configure multiple slaves and running these jenkins jobs on those slaves attached to inorder to coonect a linux agent as slave to the jenkins , we need to go the node add a new node i need to pass the ip of the slave which i need to attach as a slave i need to add the pem file of the particular slave ineed to pass the user directory and i need to select all the tpye of checks that jenkins need to be providing while connecting to the particular slave.

Q: explain ci/cd pieplines?

ans:we have multiple stages in ci cd pipelines and these would be trigged via a webhook we have configuured.
whenever developer creates pull request this would be triggaring the jenkins pipeline via webhook where would be having multiple stages, and the first stage is checkout stage where would be checking out all of the latest code the would be building artifact second stage then we would be doing the sonarscans to fix the buggs in that particular projects  next stage we would be building docker file and we would push the docker file and images in kubernetes cluster and we would be upgarding our DEV and QA server with latest image 
we would be running our QA automation test cases on top of newly released build and sending the results post build actions to the developer as well as QA team and we have used multiple plugins this pipeline in order store the jenkins credentials and we had use jenkins credentials plugin by using by usting the credentials id in these stages we were able to check out this repositories.