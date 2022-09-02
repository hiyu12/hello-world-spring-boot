pipeline{
    agent any
    tools{
        maven 'maven'
        Docker 'docker-1.2'
    }
    stages{
        stage('Git Clone'){
            steps{
                git 'https://github.com/hiyu12/hello-world-spring-boot.git'
            }
        }
        stage('Maven Build'){
            steps{
                sh 'mvn --version'
                sh 'mvn package'
            }
        }
        stage('DockerDeploy'){
            steps{
                sh 'docker --version'
                sh 'docker build -t akash5791/springboot:latest .'
            }
        }
    }
}
