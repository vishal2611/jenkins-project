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
        }

        failure {
            echo "Pipeline failed"
        }
    }
}
