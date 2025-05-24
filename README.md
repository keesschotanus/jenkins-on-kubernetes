# jenkins-on-kubernetes
Jenkins jobs using Jenkins running on Kubernetes

# The Jobs

## Hello World!

The job is stored in the file: Jenkinsfile-hello-world

This is a simple pipeline job that you should be able to paste and then run.
- Click "+ New Item", and name your job.
- Select the "Pipeline" icon and click "OK".
- Now paste the code above in the "Script" section.

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
