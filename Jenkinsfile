pipeline {
    agent any

    triggers {
        cron('H/10 * * * 1') // Trigger every 10 minutes on Mondays
    }

    stages {
        stage('Build') {
            steps {
                // Add steps to build your project
                bat "mvn clean package" 
            }
        }

        stage('Generate Code Coverage Report') {
            steps {
                // Add steps to generate code coverage report with Jacoco
                bat "mvn jacoco:report"
            }
        }
    }
}
