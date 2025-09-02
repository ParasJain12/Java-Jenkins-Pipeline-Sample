pipeline {
    agent any

    tools{
        maven "maven"
    }
    
    environment{
        VERSION_NAME="1.34"
    }
    stages {
        stage("compile") {
            steps {
                bat 'javac Main.java'
                echo "${VERSION_NAME}"
            }
        }

        stage("run") {
            steps {
                bat 'java Main'
            }
        }
    }

    post {
        always {
            echo "Build Always"
        }
        success {
            echo "Build Success"
        }
        failure {
            echo "Build Failure"
        }
    }
}
