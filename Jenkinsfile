pipeline {
    environment {
        CI = 'true'
    }
    stages {
        stage('Build') {
            steps {
                echo build
            }
        }
        stage('Test') {
            steps {
                echo test
            }
        }
        stage('Deliver for development') {
            when {
                branch 'development' 
            }
            steps {
                echo development
            }
        }
        stage('Deploy for production') {
            when {
                branch 'production'  
            }
            steps {
                echo production
            }
        }
    }
}
