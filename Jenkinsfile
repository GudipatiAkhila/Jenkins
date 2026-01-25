pipeline {
    agent {                               // pre-build
        node{
            label 'AGENT-1'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh """
                   echo "Building"

                """
            }
        }
        stage('Test') {                    // build
            steps {
                  sh """
                   echo "Testing"

                """
                
            }
        }
        stage('Deploy') {
            steps {
                sh """
                    echo "Deploying"
                """
            }
        }
    }
    post {
        always {
            echo 'I will always say Hello again'  // this step is for it will execute even pipeline failed case also.
            cleanWs()                             //clean the workspace after the build finishes whther it may be failes / sucess

        }
        success {
            echo 'I will run if success'            // podt build
        }
        failure {
            echo 'I will run if failure'   
        }
    }
}