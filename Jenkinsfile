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

        stage("Compile") {
            steps {
                sh 'mvn compile'
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

        stage("Archive Artifacts") {
            steps {
                archiveArtifacts allowEmptyArchive: true, artifacts: 'target/*.jar', followSymlinks: false, onlyIfSuccessful: true
            }
        }
    }
}
