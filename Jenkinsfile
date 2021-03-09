pipeline {
    agent any
    stages {
        stage('Test') {
            steps{
                bat 'dir'
            }
        }
    }
    post {
        failure {
            mail bcc: '', body: "$BUILD_NUMBER is $currentBuild.currentResult", subject: "$JOB_NAME", to: 'sakshipatmase@gmail.com'
        }
        success {
            mail bcc: '', body: "$BUILD_NUMBER is $currentBuild.currentResult", subject: "$JOB_NAME", to: 'sakshipatmase@gmail.com'
        }      
    }
}