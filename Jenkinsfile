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
        stage('deploying the file to tomcat server'){
            steps {
                sh 'sudo scp /var/lib/jenkins/workspace/Mahidhar-Github_war-demo_main/target/webapp.war 35.182.254.65:/usr/share/tomcat/webapps'
            }
        }
    }
}