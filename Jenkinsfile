// Jenkinsfile
pipeline {
    agent any // This means Jenkins can use any available agent/node to run this pipeline.

    stages {
        stage('Checkout Code') {
            steps {
                // This stage is mostly for show, as Jenkins automatically checks out the code first.
                echo '✅ Code checkout is handled by Jenkins SCM configuration.'
            }
        }

        stage('Build') {
            steps {
                // Installs all the necessary packages from your package.json
                sh 'npm install'
                echo '🏗️ Project dependencies installed successfully!'
            }
        }

        stage('Test') {
            steps {
                // Runs the test script defined in your package.json
                sh 'npm test'
                echo '🧪 All tests passed!'
            }
        }

        stage('Deploy') {
            steps {
                // This is a placeholder for your actual deployment commands.
                echo '🚀 Deploy step placeholder.'
                // sh './deploy.sh' 
            }
        }
    }

    post {
        // This block runs after all stages are complete.
        always {
            echo 'Pipeline finished.'
        }
        success {
            echo '🎉 Hooray! The pipeline succeeded!'
        }
        failure {
            echo '❌ Oh no, the pipeline failed.'
        }
    }
}