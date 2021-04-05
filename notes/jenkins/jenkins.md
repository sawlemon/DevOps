#  Jenkins


[Install Jenkins in Ubuntu](https://www.jenkins.io/doc/book/installing/linux/#debianubuntu)

*Install java and then install Jenkins*

or simply go for docker image

[Official Jenkins Docker image](https://github.com/jenkinsci/docker/blob/master/README.md)

    docker run -d -p 8080:8080 -p 50000:50000 -v jenkins_home:/var/jenkins_home jenkins/jenkins:lts

[Jenkins Full Course | Jenkins Tutorial For Beginners | Jenkins Tutorial | Simplilearn](https://youtu.be/FX322RVNGj4)


## Plugins

[Plugins Index](https://plugins.jenkins.io/)

![](images/2020-12-18-13-23-05.png)



[LDAP](https://plugins.jenkins.io/ldap/)

[Role-based Authorization Strategy](https://plugins.jenkins.io/role-strategy/)


[Credentials](https://plugins.jenkins.io/credentials/)

[Deploy to container](https://plugins.jenkins.io/deploy/)

[Blue Ocean for Jenkins Pipelines](https://www.jenkins.io/projects/blueocean/)
    Different UI in Jenkins

[GitHub Integration](https://plugins.jenkins.io/github-pullrequest/)


[Integrate with GitHub: build after each commit (Get started with Jenkins, part 13)](https://youtu.be/Z3S2gMBUkBo)    

[30 Jenkins features and plugins you wished you had known about before! by Joep Weijers](https://youtu.be/6BIry0cepz4)

[Complete Jenkins Pipeline Tutorial | Jenkinsfile explained](https://youtu.be/7KCS70sCoK0)

[Set Up a Jenkins Build Server -AWS ](https://d1.awsstatic.com/Projects/P5505030/aws-project_Jenkins-build-server.pdf)

[Pipeline: AWS Steps](https://plugins.jenkins.io/pipeline-aws/)

[Jenkins Master to Launch AWS EC2 instances as Slaves using EC2 plugin](https://youtu.be/1XI9_4umWVk)
 
[Run bash command on jenkins pipeline](https://stackoverflow.com/questions/44330148/run-bash-command-on-jenkins-pipeline)

    stage('Setting the variables values') {
        steps {
            sh '''#!/bin/bash
                    echo "hello world" 
            '''
            }
    }

[command not found from Jenkins Execute Shell](https://stackoverflow.com/questions/46199123/command-not-found-from-jenkins-execute-shell#:~:text=Add%20the%20path%20to%20the,%3E%20Configure%20System%2C%20Global%20Properties.&text=Call%20the%20eb%20command%20with%20its%20fully%20qualified%20path.)

    
    Your Jenkins setup has a different path than the user you logged in with.

    There are two solutions:

    Add the path to the executable in the PATH environment variable. Use where eb to find the correct path. Then in Jenkins, click on Manage Jenkins -> Configure System, Global Properties. Check Environment Variables. Set Name to PATH. Set Value to $PATH:/path/to/eb. Then restart Jenkins.

    Call the eb command with its fully qualified path.

[Jenkins - Build & Publish Docker Images](https://youtu.be/6tcoRIPBd8s)

