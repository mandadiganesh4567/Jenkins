pipeline {
    agent {
          node {
            label 'AGENT1'
          }
    }
    stages {
        stage('Build') {
            steps {
                script{
                    sh """
                            echo "Building"
                    """
                 }
            }
        }
        stage('Test') {
            steps {
                script {
                    sh """
                
                echo " Testing"
                """
            }
        }
        }
        stage('Deploy') {
            steps {
                script {
                    sh """
                
                echo " Deploying"
                """
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
}