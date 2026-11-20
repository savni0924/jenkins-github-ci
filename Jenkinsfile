pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the web application'
                bat 'dir'
            }
        }

        stage('Test') {
            steps {
                script {
                    if (fileExists('index.html')) {
                        echo 'Application file found!'
                    } else {
                        error 'Application file missing!'
                    }
                }
            }
        }

        stage('Success') {
            steps {
                echo 'Build completed successfully!'
            }
        }
    }
}
