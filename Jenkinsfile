pipeline {
    agent any
    stages {
        stage {
            steps {
                echo 'Hello World'
            }
        }    
        stage ('pull code') {
            steps {
                git credentialsId: 'user', url: 'https://github.com/saurabh-786-user/aws-sample-cicd-cdk-1.git'
            }
        } 
        stage('deploy') {
            steps {
                sh 'docker build -t php:v1 .'
                sh 'docker-compose up'
            }    
        }
    }
}
