pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                script {
                    // Pulling the source code from the GitHub repository using curl
                    sh 'curl -L https://github.com/Harrydmc/simple-node-js-react-npm-app/archive/refs/heads/main.tar.gz | tar zx'
                    // Change directory to the downloaded repository
                    dir('simple-node-js-react-npm-app-main') {
                        // Install dependencies
                        sh 'npm install'
                    }
                }
            }
        }
    }
}
