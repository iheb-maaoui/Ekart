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

        stage("Test the maven project") {
            steps {
                script {
                    sh "mvn clean test -DskipITs"
                }
            }
        }

        stage("Install app to the local maven repo") {
            steps {
                sh "mvn install -DskipTests"
            }
        }
    }
}