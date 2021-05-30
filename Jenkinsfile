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
                sh 'sudo scp -i /home/ec2-user/honey.pem /var/lib/jenkins/workspace/Mahidhar-Github_war-demo_main/target/webapp.war ec2-user@172.31.10.157:/usr/share/tomcat/webapps'
            }
        }
    }
}