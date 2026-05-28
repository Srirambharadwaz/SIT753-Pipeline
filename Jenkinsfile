pipeline {
    agent any

    options {
        timeout(time: 2, unit: 'MINUTES')
    }

    stages {

        stage('Build') {
            steps {
                echo 'Building application using Maven...'
                sleep(time: 10, unit: 'SECONDS')
            }
        }

        stage('Unit and Integration Tests') {
            steps {
                echo 'Running JUnit and Selenium tests...'
                sleep(time: 10, unit: 'SECONDS')
            }
        }

        stage('Code Analysis') {
            steps {
                echo 'Running SonarQube analysis...'
                sleep(time: 10, unit: 'SECONDS')
            }
        }

        stage('Security Scan') {
            steps {
                echo 'Running OWASP Dependency Check...'
                sleep(time: 10, unit: 'SECONDS')
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo 'Deploying to AWS staging environment...'
                sleep(time: 10, unit: 'SECONDS')
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                echo 'Running staging integration tests...'
                sleep(time: 10, unit: 'SECONDS')
            }
        }

        stage('Deploy to Production') {
            steps {
                echo 'Deploying to production...'
                sleep(time: 10, unit: 'SECONDS')
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully within 2 minutes.'
        }

        failure {
            echo 'Pipeline failed or exceeded 2-minute timeout.'
        }
    }
}
