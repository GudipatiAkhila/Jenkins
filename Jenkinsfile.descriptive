pipeline {
    agent {
        node{
            label 'AGENT'
        }
    }
    stages {
        stage('Build') {
            steps {
                echo "Building"
            }
        }
        stage('Test') {
            steps {
                echo "Testing"
            }
        }
        stage('Deploy') {
            steps {
                echo "Deploying"
            }
        }
    }
    post {
        always {
            echo 'I will always say Hello again'  // this step is for it will execute even pipeline failed case also.
            cleanWs()
        }
        success {
            echo 'I will run if success'
        }
        failure {
            echo 'I will run if failure'   
        }
    }
}