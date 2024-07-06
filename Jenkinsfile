pipeline {
    agent any

    stages {
        stage("Verify checkout") {
            steps {
                echo "Checking out from the SCM"
                script {
                    sh "ls -al"
                }
            }
        }
    }
}