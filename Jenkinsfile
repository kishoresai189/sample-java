pipeline {
    agent any

    stages {
        stage('Build') {
            when {
                // Define the condition for triggering the build
                branch 'main'
                branch 'master'
                branch 'feature/*'
            }
            steps {
                sh 'mvn clean install'
            }
        }
    }
}
