pipeline {
    agent any
    stages {
        stage('Performance Testing') {
            steps {
                echo 'Installing k6'
                bat 'sudo chmod +x setup_k6.bat'
                bat 'sudo ./setup_k6.bat'
                echo 'Running K6 performance tests...'
                sh 'k6 run loadtests/performance-test.js'
            }
        }
    }
}
