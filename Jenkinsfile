pipeline {
    agent any
    stages {
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
