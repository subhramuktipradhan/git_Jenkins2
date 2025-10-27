pipeline {
    agent any

    environment {
        python = 'C:\\Users\\Subhra\\AppData\\Local\\Programs\\Python\\Python314\\python.exe'
    }

    stages {
        stage('checkout code') {
            steps {
                checkout scm
            }
        }

        stage('extract data') {
            steps {
                bat "${python} extract.py"
            }
        }
    }

    post {
        success {
            echo 'success..'
        }
        failure {
            echo 'failure'
        }
        always {
            echo 'always'
        }
    }
}
