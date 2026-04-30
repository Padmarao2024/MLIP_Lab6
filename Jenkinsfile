pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                bat '''
                echo In C or Java, we can compile our program in this step
                echo In Python, we can build our package here or skip this step
                '''
            }
        }
        stage('Test') {
            steps {
                bat 'C:\\Users\\abhil\\anaconda3\\Scripts\\conda.exe run -n mlip pytest'
            }
        }
        stage('Deploy') {
            steps {
                echo 'In this step, we deploy our project'
                echo 'Depending on the context, we may publish the project artifact or upload pickle files'
            }
        }
    }
    post {
        always {
            echo 'Pipeline finished.'
        }
        success {
            echo 'All tests passed!'
        }
        failure {
            echo 'Tests failed.'
        }
    }
}
