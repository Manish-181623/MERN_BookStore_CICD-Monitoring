pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello Hello Hello This is a pipeline'
            }
        }  
        stage('Clone') {
            steps {
                checkout scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/Manish-181623/MERN_BookStore_CICD-Monitoring.git']])
            }
        }
        stage('Run') {
            steps {
                sh 'sudo docker-compose up -d'
            }
        }   
    }
  
}
