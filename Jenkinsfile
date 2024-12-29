pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                checkout scm
            }
        }
        stage('Execute Bash Script') {
            steps {
                script {
                    if (isUnix()) {
                        sh './list_files.sh'  // Use sh for Unix-like systems (including WSL or Git Bash on Windows)
                    } else {
                        bat 'bash ./list_files.sh'  // Use bat for running bash scripts on Windows
                    }
                }
            }
        }
    }
}
