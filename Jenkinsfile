@Library('jenkins-libraries') _
pipeline {
    agent any
    stages {
        stage ('Detect Change') {
            when {
                expression {env.BRANCH_NAME == 'main'}
            }
            steps {
                script {
                    sh 'git diff --name-only main test'
                }
            }
        }
    }
}
