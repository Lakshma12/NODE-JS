pipeline {
    agent any
    
    environment {
        // Define environment variables
        GIT_REPO_URL = 'https://github.com/Lakshma12/NODE-JS.git'  // Repository URL
        BRANCH_NAME = 'main'  // Branch to clone
    }

    stages {
        stage('Checkout') {
            steps {
                // Clone the repository
                git branch: "${BRANCH_NAME}", url: "${GIT_REPO_URL}"
            }
        }
        
        stage('Install Dependencies') {
            steps {
                // If you have a package.json, install dependencies
                script {
                    sh 'npm install'
                }
            }
        }

        stage('Run Node.js Script') {
            steps {
                // Run the Node.js app.js script
                script {
                    sh 'node app.js'  // Running app.js script
                }
            }
        }
    }

    post {
        always {
            // This block will always run, whether the pipeline succeeds or fails
            echo 'Pipeline finished.'
        }
    }
}
