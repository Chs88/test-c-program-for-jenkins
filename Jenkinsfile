pipeline {
    agent any

    stages {

        stage("Checkout Codebase") {

            steps {

                checkout scm: [$class: "GitSCM", userRemoteConfigs: [[credentialsId: "github-ssh-key", url: "git@github.com:Chs88/test-c-program-for-jenkins.git"]]]
            }   //checks out using the scm tag (source code management) it uses SSH creds previously added to Github and Jenkins

        }


        steps("Build") {

            steps {
                sh "gcc mt-example-0.c -lpthread"
            }
        }

        stage("test") {

            steps {
                sh "./a.out"
            }


    }

        stage("deploy") {
            steps{

            sh "echo done!!!"
            }
        }



}