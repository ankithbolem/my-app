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
                environment name: 'qa_TO', value: 'qa'
            }
            steps {
                sh 'mvn clean package'
            }
        }
        stage('tomcat-deploy') {
            when {
                branch 'production'
                environment name: 'production_TO', value: 'production'
            }
            steps {
            echo "hello this is tom cat deploy"
            }
        }
    }
}
