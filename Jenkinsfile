pipeline {
    agent any

    stages {
        stage('Stage 1') {
            steps {
                echo 'Checking out source code...'
                git url: 'https://github.com/PrashansaPokhrel/Jenkins-Pipeline.git', branch: 'main'
            }
        }
        
        stage('Build') {
            steps {
                echo 'Building the project...'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
            }
        }
    }
}
