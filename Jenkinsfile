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
            echo "Pipeline pass"
            mail to : "worthinwords26@gmail.com",
            subject : "SUCCESS",
            body : "Email working"
        }

        failure {
            echo "Pipeline failed"
        }
    }
}
