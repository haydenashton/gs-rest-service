pipeline {
    agent { docker { image 'maven:3.3.3' } }
    stages {
        stage('build') {
            steps {
                sh 'mvn clean install'
            }
        }
        stage('deploy') {
            steps {
                sh 'pwd'
                sh 'mvn -e -X clean compile org.apache.tomcat.maven:tomcat7-maven-plugin:deploy'
            }
        }
    }
}
