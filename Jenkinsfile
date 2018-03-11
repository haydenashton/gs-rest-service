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
                sh 'cat pom.xml'
                sh 'mvn -e -X org.apache.tomcat.maven:tomcat7-maven-plugin:deploy'
            }
        }
    }
}
