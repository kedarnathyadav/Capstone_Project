pipeline {
    agent any
    environment{
        PATH ="/opt/maven/apache-maven-3.8.3/bin:$PATH"
    }
    stages {
        stage('Git Clone') {
            steps {
                git branch: 'main', url: 'https://github.com/kedarnathyadav/Capstone_Project.git'
            }
        }
        stage('Build') {
            steps {
               sh "mvn clean install"
            }
        }
        stage('Deploy') {
            steps {
                sh "mvn tomcat7:run"
            }
        }
    }
}
