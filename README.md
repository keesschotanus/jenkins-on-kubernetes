# jenkins-on-kubernetes
Jenkins jobs using Jenkins running on Kubernetes

# The Jobs

## Hello World!

This is a simple pipeline job that you should be able to paste and then run.
- Click "+ New Item", and name your job.
- Select the "Pipeline" icon and click "OK".
- Now paste the code from the file: Jenkinsfile-hello-worldabove, in the "Script" section.

To make it slightly more interesting you can fetch the job from GitHub.
- Click "+ New Item", and name your job.
- Select the "Pipeline" icon and click "OK".
- In the "Pipeline" section and then "Definition", click on the drop-down and select "Pipeline script from SCM"
- Now enter the following data:

| Field            | Value                                                  |
|------------------|--------------------------------------------------------|
| SCM              | Git                                                    |
| Repository URL   | https://github.com/keesschotanus/jenkins-on-kubernetes | 
| Branch Specifier | **/main                                                | 
| Script Path      | Jenkinsfile-hello-world                                |  

Again you should be able to run this job, but now the Jenkins job in the
Jenkinsfile-hello-world file is fetched from GitHub before being executed.

## Container Mix

The "Hello World" jobs run in the default container named jnlp.
It has limited resources and limited available tools.
Let's see if we can use different containers.
In this case a Maven and a NodeJS container.

For this job we have a Jenkins file named: Jenkinsfile-container-mix
and a pod definition file named: Jenkinsfile-container-mix.pod.yaml.
Check them out.

Creating this job is similar to the "Hello World!" job where the Jenkins job is fetched from GitHub.
- Click "+ New Item", and name your job.
- Select the "Pipeline" icon and click "OK".
- In the "Pipeline" section and then "Definition", click on the drop-down and select "Pipeline script from SCM"
- Now enter the following data:

| Field            | Value                                                  |
|------------------|--------------------------------------------------------|
| SCM              | Git                                                    |
| Repository URL   | https://github.com/keesschotanus/jenkins-on-kubernetes | 
| Branch Specifier | **/main                                                | 
| Script Path      | Jenkinsfile-container-mix                              |  

When you run this job you should see the latest version of node and maven in the console output. 
