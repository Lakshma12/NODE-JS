pipeline {
    agent any
    
    environment {
        // Define environment variables
        GIT_REPO_URL = 'https://github.com/Lakshma12/NODE-JS.git'  // Repository URL
        BRANCH_NAME = 'main'  // Replace with the branch you want to clone
    }

    stages {
        stage('Checkout') {
            steps {
                // Clone the repository
                git branch: "${BRANCH_NAME}", url: "${GIT_REPO_URL}"
            }
        }
        
        // Add other stages like build, test, or deploy if needed
    }

    post {
        always {
            // This block will always run, whether the pipeline succeeds or fails
            echo 'Pipeline finished.'
        }
    }
}
