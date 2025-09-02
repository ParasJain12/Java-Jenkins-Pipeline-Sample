pipeline{
    agent any
    stages{
        stage("compile"){
            steps{
                bat 'javac Main.java'
            }
        }

        stage("run"){
            steps{
                bat 'java Main'
            }
        }
    }

    post{
        always{
            bat "Build Always"
        }
        success{
            bat "Build Success"
        }
        failure{
            bat "Build failure"
        }
    }
}
