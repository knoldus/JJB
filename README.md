# Jenkins Job Builder

Jenkins Job Builder takes simple descriptions of Jenkins jobs in YAML or JSON format and uses them to configure Jenkins. 

You can keep your job descriptions in human readable text format in a version control system to make changes and auditing easier.

I'm going to use YAML format for creating the Jenkins Pipeline using Jenkins Job Builder.


#### To install:

`pip install --user jenkins-job-builder`


#### Test a job definition:

JJB creates Jenkins XML configuration file from a YAML/JSON definition file and just uploads it to Jenkins.

`jenkins-jobs test jjb1.yaml`

`jenkins-jobs test jjb2.yaml`



#### Updating Jenkins Jobs:


Once you’ve tested your job definition and are happy with it then you can use the update command to deploy the job to Jenkins. 


`jenkins-jobs update jjb1.yaml`

`jenkins-jobs update jjb2.yaml`



####  Deleting a job:


`jenkins-jobs delete jjb2.yaml`



#### Providing plugins info:

To generate a plugins info, using an account with Administrator rights:

`jenkins-jobs get-plugins-info -o plugins_info.yaml`
