pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh '''
                    ls -la
                    node --version
                    npm --version
                    npm ci
                    npm run build
                    ls -la
                '''
            }
        }
        
        stage('Test') {
            steps {
                echo 'Test stage'
            }
        }
    }
    
    post {
        always {
            // Archive JUnit test results if available
            junit 'test-results/results.xml'
        }
    }
}
