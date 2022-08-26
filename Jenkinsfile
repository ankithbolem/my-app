pipeline {
    agent any
    stages {
        stage('git checkout') {
            steps {
                git branch: 'dev', credentialsId: '123', url: 'https://github.com/ankithbolem/my-app'
            }
        }
        stage('maven build') {
            when {
                branch 'dev'
            }
            steps {
                sh 'mvn clean package'
            }
        }
        stage('tomcat-deploy') {
            when {
                branch 'devlop'
            }
            steps {
            echo "hello this is tom cat deploy"
            }
        }
    }
}
