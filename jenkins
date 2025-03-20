pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Starting Build Stage'
                sh 'g++ -o YOUR_SRN-1 your_file.cpp' // Compiling the C++ file
                echo 'Build Stage Successful'
            }
        }

        stage('Test') {
            steps {
                echo 'Running Tests'
                sh './YOUR_SRN-1' // Executing the compiled C++ program
                echo 'Test Stage Successful'
            }
            post {
                always {
                    echo 'Simulated test reports generated'
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying Application'
                sh 'echo Deploy simulation' // Placeholder for actual deployment
                echo 'Deployment Successful'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed! Check logs for errors.'
        }
    }
}
