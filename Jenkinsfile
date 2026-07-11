pipeline {
    agent {
        label 'electronix'
    }

    stages {
        stage('Hello') {
            steps {
                echo "Hello Jenkins"
            }
        }

        stage('Hello-Second') {
            steps {
                echo "Hello Jenkins second"
            }
        }
    }

    post {
        success {
            echo "Pipeline Pass"

            mail(
                to: "worthinwords26@gmail.com",
                subject: "SUCCESS: Job '${env.JOB_NAME} [${env.BUILD_NUMBER}]'",
                body: "${env.JOB_NAME} Build Succeeded.\n\nCheck Build URL: ${env.BUILD_URL}"
            )
        }

        failure {
            echo "Pipeline Failed"

            mail(
                to: "worthinwords26@gmail.com",
                subject: "FAIL: Job '${env.JOB_NAME} [${env.BUILD_NUMBER}]'",
                body: "${env.JOB_NAME} Build Failed.\n\nCheck Build URL: ${env.BUILD_URL}"
            )
        }
    }
}
