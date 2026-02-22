pipeline {
    agent {
          node {
            label 'AGENT1'
          }
    }
    environment {
        Course = 'jenkins'
    }
    options {
        timeout (time: 10, unit: 'SECONDS')
        disableConcurrentBuilds()
    }
    stages {
        stage('Build') {
            steps {
                script{
                    sh """
                            echo "Building"
                            echo 'Im learning $Course'
                            env
                            #sleep 10
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
        aborted {
            echo 'Pipeline is aborted'
        }
        
    }
}
