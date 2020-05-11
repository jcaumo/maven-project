pipeline {
    agent { label 'Staging'}
    tools {
        maven 'localMaven'
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn clean package'
                sh "docker build . -t tomcatweapp:${env.BUILD_ID}"
            }
        }
    }
}