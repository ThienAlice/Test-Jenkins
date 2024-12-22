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
                    def change = myLibrary.detectChange("${env.BRANCH_NAME}", "main")
                    if (change == "") {
                        echo "No changes detected. Exiting..."
                    }
                    else {
                        echo "Changes detected: ${change}"
                    }
                }
            }
        }
    }
}
