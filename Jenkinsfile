pipeline {
    agent any
    stages{
        stage('cleaning the file'){
            step  {
               sh 'mvn clean'
                }
        }
        stage('testing the project'){
            step {
                sh 'mvn test'
            }
        }
        stage('build'){
            step {
                sh 'mvn package'
            }
        }
    }
}