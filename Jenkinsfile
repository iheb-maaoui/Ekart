pipeline {
    agent any

    stages {
        stage("Checkout from SCM") {
            steps {
                echo "Checking out from the SCM"
                checkout scmGit(branches: [[name: 'main']], extensions: [], userRemoteConfigs: [[credentialsId: 'github-username-password', url: 'https://github.com/iheb-maaoui/Ekart.git']])
                ls -al
            }
        }
    }
}