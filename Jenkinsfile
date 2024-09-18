pipeline {
    agent any
    stages {
        stage('Initialize Repositories') {
            steps {
                script {
                    echo "Main repository cloned at: ${env.WORKSPACE}"
                    sh 'pwd'
                    sh 'ls -la'
                    def secondRepoDir = "${env.WORKSPACE}/telegram_bot_base"
                    if (fileExists(secondRepoDir)) {
                        echo "Second repository cloned at: ${secondRepoDir}"
                        dir(secondRepoDir) {
                            sh 'ls -la'
                        }
                    } else {
                        echo "Second repository directory not found!"
                    }
                }
            }
        }
    }
}
