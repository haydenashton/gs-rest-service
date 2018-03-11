pipeline {
    agent { docker { image 'jenkins-maven-slave' } }
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
