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
                    sh 'git fetch origin main'
                    sh 'git fetch origin test'
                    sh 'git branch -r'
                    sh 'git diff --name-only origin/main origin/test --'
                }
            }
        }
    }
}
