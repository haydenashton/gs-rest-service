pipeline {
    agent { docker {
      # image 'maven:3.3.3'
      image 'localhost/jenkins-maven-slave'
    } }
    stages {
        stage('build') {
            steps {
                sh 'mvn clean install'
            }
        }
        stage('deploy') {
            steps {
                sh 'mvn tomcat7:deploy'
            }
        }
    }
}
