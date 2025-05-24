pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the application...'
                sh 'mvn clean package' // Using Maven
            }
        }
        
        stage('Unit and Integration Tests') {
            steps {
                echo 'Running unit and integration tests...'
                sh 'mvn test' // Using JUnit & Selenium
            }
        }

        stage('Code Analysis') {
            steps {
                echo 'Analyzing code for quality and standards...'
                sh 'sonar-scanner' // Using SonarQube
            }
        }

        stage('Security Scan') {
            steps {
                echo 'Performing security scan...'
                sh 'dependency-check.sh --project Jenkins-Pipeline --scan .' // OWASP Dependency-Check
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo 'Deploying to Staging environment...'
                sh 'scp target/app.jar user@staging-server:/deploy/' // AWS EC2
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                echo 'Running integration tests on staging...'
                sh 'postman run staging_tests.json' // Using Postman & Selenium
            }
        }

        stage('Deploy to Production') {
            steps {
                echo 'Deploying to Production...'
                sh 'scp target/app.jar user@production-server:/deploy/' // AWS EC2
            }
        }
    }
}