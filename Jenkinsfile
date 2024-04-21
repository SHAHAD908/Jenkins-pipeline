pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                // Perform build tasks here
            }
        }

        stage('Unit and Integration Tests') {
            steps {
                echo 'Running unit tests on JUnit...'
                echo 'Running integration tests on JUnit...'
                // Simulate unit and integration tests
            }
            post {
                success {
                    mail to: 'shahad908.556@gmail.com',
                         subject: 'Tests Passed',
                         body: 'All tests passed successfully.'
                }
                failure {
                    mail to: 'shahad908.556@gmail.com',
                         subject: 'Test Failures',
                         body: 'Some tests failed. Review the test results.'
                }
            }
        }

        stage('Code Analysis') {
            steps {
                echo 'Performing code analysis. Executing SonarQube analysis using SonarScanner.'
                // Perform code analysis tasks
            }
        }

        stage('Security Scan') {
            steps {
                echo 'Performing security scan through OWASP ZAP (Zed Attack Proxy)...'
                // Perform security scan tasks
            }
            post {
                success {
                    mail to: 'shahad908.556@gmail.com',
                         subject: 'Security Scan Passed',
                         body: 'No security vulnerabilities found.'
                }
                failure {
                    mail to: 'shahad908.556@gmail.com',
                         subject: 'Security Scan Failed',
                         body: 'Security vulnerabilities detected. Take action.'
                }
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo 'Deploying the application to a staging server (e.g., AWS EC2 instance'
                // Deploy to staging tasks
            }
            
        }

        stage('Integration Tests on Staging') {
            steps {
                echo 'Running integration tests on staging...'
                // Simulate integration tests on staging
            }
            post {
                success {
                    mail to: 'shahad908.556@gmail.com',
                         subject: 'Integration Tests on Staging Passed',
                         body: 'Integration tests on staging passed.'
                }
                failure {
                    mail to: 'shahad908.556@gmail.com',
                         subject: 'Integration Tests on Staging Failed',
                         body: 'Integration tests on staging failed. Investigate.'
                }
            }
        }

        stage('Deploy to Production') {
            steps {
                echo 'Deploy the application to a production server (e.g., AWS EC2 instance)..'
                // Deploy to production tasks
            }
        }
        stage('Complete') {
            steps {
                echo 'New stage after commit..'
                // Deploy to production tasks
            }
        }
    }
}
