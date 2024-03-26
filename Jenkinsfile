pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    def branchName = env.BRANCH_NAME ?: 'master'
                    if (branchName == 'main' || branchName == 'master' || branchName.startsWith('feature/')) {
                        sh 'mvn clean install'
                    } else {
                        echo "Skipping build for branch: ${branchName}"
                    }
                }
            }
        }
    }
}

