pipeline {
    agent {
          node {
            label 'AGENT1'
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
                echo " Testing"
            }
        }
        stage('Deploy') {
            steps {
                echo "Deploying"
            }
        }
    }
    post {

        always
        {
            echo " I will always say Hello !!!"
            cleanWs()
        }
        success {
            echo 'Code is SUCCESS!!'
        }
        failure {
            echo 'code is Failure!!'
        }
    }
}