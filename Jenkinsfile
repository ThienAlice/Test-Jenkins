@Library('jenkins-libraries') _
pipeline {
    agent any
    stages {
        stage ('for pull request') {
            when {
                changeRequest()
            }
            steps {
                script {
                    echo "${env.BRANCH_NAME}"
                }
            }
        }
        stage ('Detect Change') {
            when {
                expression {env.BRANCH_NAME == 'main'}
            }
            steps {
                script {
                    echo "${env.BRANCH_NAME}"
                }
            }
        }
    }
}
