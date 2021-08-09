//Declarative pipeline

pipeline {
    agent any 
    tools {
        maven 'Maven-3.8.1' 
    }
    stages {
        stage('Checkout') { 
            steps {
		git 'https://github.com/zaynazar/myapp01.git'
                
            }
        }
        stage('Build') { 
            steps {
                sh 'mvn clean package'
            }
        }
        stage('Notification') { 
            steps {
                echo "successfully deployed through SCM"
            }
        }
    }
}
