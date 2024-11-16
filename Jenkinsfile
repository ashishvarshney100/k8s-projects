pipeline {
    agent any
    tools {
        maven 'maven3'
    }
    stages {
        stage("Code Cloning"){
            steps{
                sh 'echo "Code is clonning"'
                git changelog: false, poll: false, url: 'https://github.com/ashishvarshney100/Ekart.git'
            }
        }
        stage("Build"){
            steps{
                sh 'echo "Code is Building"'
                sh 'mvn clean compile'
                sh 'mvn clean install'
            }
        }
        stage("Test"){
            steps{
                sh 'echo "Testing the code"'
            }
        }
        stage("Deploy"){
            steps{
                sh 'echo "Deploying the code"'
            }
        }
    }
}
