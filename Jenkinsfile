pipeline {
    environment {
        CI = 'true'
    }
    stages {
        stage('Build') {
            steps {
				stage('scm checkout'){
				git 'https://github.com/pushpen12/spring-project.git'				 
				def mvnHome = tool name: 'M2_HOME', type: 'maven'
				def mvnCMD = "${mvnHome}/bin/mvn"
				sh "${mvnCMD} clean package -Dskiptests"
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
}
