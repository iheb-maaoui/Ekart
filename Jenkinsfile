@Library('custom-pipeline') _

pipeline {
    agent any
    stages {

        stage("Print the build number") {
            steps {
                printBuildNumber("test1", "test2")
            }
        }

        stage("Say hello") {
            steps {
                echoHello()
            }
        }
    }
}
