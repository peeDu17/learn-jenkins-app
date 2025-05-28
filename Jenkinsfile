stage('Test') {
    steps {
        sh 'npx playwright test'
    }
    post {
        always {
            junit 'test-results/results.xml'
        }
    }
}
