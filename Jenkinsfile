pipeline {
    agent any
    stages {
        stage('Build') { 
            steps {
                script {
                    // Detect the operating system
                    def isUnix = isUnix()

                    // Execute npm install using the appropriate step based on the OS
                    if (isUnix) {
                        sh 'npm install'
                    } else {
                        bat 'npm install'
                    }
                }
            }
        }
    }
}
