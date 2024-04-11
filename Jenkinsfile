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
        stage('Test') {
            steps {
                script {
                    // Detect the operating system
                    def isUnix = isUnix()

                    // Execute test.sh using the appropriate step based on the OS
                    if (isUnix) {
                        sh './jenkins/scripts/test.sh'
                    } else {
                        bat '.\\jenkins\\scripts\\test.bat'
                    }
                }
            }
        }
    }
}
