pipeline {
    agent { label 'java_agent' } // Use the configured agent

    stages {
        stage('Display Workspace Contents') {
            steps {
                echo "Listing workspace contents..."
                sh 'ls -lah'  // Show directory contents
            }
        }

        stage('Run JavaScript File') {
            steps {
                echo "Running app.js with Node.js..."
                sh 'node app.js'  // Run the JavaScript file
            }
        }
    }

    post {
        always {
            echo "Cleaning up workspace..."
            cleanWs()  // Clean up workspace after execution
        }
    }
}

