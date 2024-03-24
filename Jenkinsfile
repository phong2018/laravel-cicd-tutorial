pipeline {
    agent any
    stages {
        stage("Verify SSH connection to server") {
            steps {
                script {
                    echo 'Verify SSH connection to server...'
                }
            }
        }
        
        stage("Verify tooling") {
            steps {
                script {
                    echo 'Verify tooling...'
                }
            }
        }
        
        stage("Clear all running docker containers") {
            steps {
                script {
                    echo 'Clear all running docker containers...'
                }
            }
        }

        stage("Start Docker") {
            steps {
                script {
                    echo 'Start Docker...'
                }
            }
        }

        stage("Run Composer Install") {
            steps {
                script {
                    echo 'Start Docker...'
                }
            }
        }

        stage("Populate .env file") {
            steps {
                script {
                    echo 'Start Docker...'
                }
            }
        }   

        stage("Run Tests") {
            steps {
                script {
                    echo 'Start Docker...'
                }
            }
        }
 
    }

    post {
        success {
            echo 'post success...'
                                           
        }
        always {
            echo 'post always...'
        }
    }
 
}
