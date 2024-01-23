pipeline {
    agent any

    environment {
        GIT_REPO_URL = 'https://github.com/pavangnanesh/jenkins.git'
        NGINX_PATH = 'C:\\Users\\P.PAVAN GNANESH\\OneDrive\\Desktop\\Nginx\\nginx-1.24.0\\html docs'
    }

    stages {
        stage('Checkout') {
            steps {
                script {
                    // Use the checkout step to clone the Git repository
                    checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: GIT_REPO_URL]]])
                }
            }
        }

        stage('Deploy to Nginx') {
            steps {
                script {
                    // Using the Jenkins workspace variable to reference files
                    bat "C:\\Users\\P.PAVAN GNANESH\\OneDrive\\Desktop\\subbadu1" '
                }
            }
        }
    }

    post {
        success {
            echo 'Pipeline succeeded! You can add additional steps here.'
        }
        failure {
            echo 'Pipeline failed! You may want to take some actions.'
        }
    }
}
