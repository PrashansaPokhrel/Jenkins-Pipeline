pipeline {
    agent any

    stages {
        stage('Stage 1 Build') {
            steps {
                echo 'building using maven'
                git url: 'https://github.com/PrashansaPokhrel/Jenkins-Pipeline.git', branch: 'main'
            }
        }
        
        stage('Stage 2 Unit and Integration Tool') {
            steps {
                echo 'Building the project...'
            }
        }

        stage('Stage 3 Code Analysis') {
            steps {
                echo 'Analyzing..'
            }
        }

        stage('Stage 4 Security Scan') {
            steps {
                echo 'Scanning....'
            }
        }
         stage('Stage 5 Deploy') {
            steps {
                echo 'Deploying the application...'
            }
        }
         stage('Stage 6 Integrating Tests') {
            steps {
                echo 'Integrating...'
            }
        }
         stage('Stage 7 Deploy Production') {
            steps {
                echo 'Deploying the application...'
            }
        }
    }
}
