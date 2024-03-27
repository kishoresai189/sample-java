pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                script {
                    git branch: 'main', url: 'https://github.com/kishoresai189/sample-java.git'
                }
            }
        }
		stage('scanning') {
            steps {
              echo " This is the scanning stage"
              sh 'sleep 5'		  
            }
        }
		stage('Test') {
            steps {
                echo " this is the test stage"
				sh 'sleep 5'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean install'
            }
        }
    }
}
