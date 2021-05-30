pipeline {
    agent any
    stages{
        stage('cleaning the file'){
            steps {
               sh 'mvn clean'
                }
        }
        stage('testing the project'){
            steps {
                sh 'mvn test'
            }
        }
        stage('build'){
            steps {
                sh 'mvn package'
            }
        }
    }
}