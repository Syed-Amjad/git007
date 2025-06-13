pipeline {
    agent any

    stages {
        stage('Clone Repo') {
            steps {
                checkout([$class: 'GitSCM',
                    branches: [[name: '*/master']],
                    userRemoteConfigs: [
                        [url: 'https://github.com/Syed-Amjad/git007.git']
                    ]
                ])
            }
        }

        stage('Build') {
            steps {
                echo 'Installing dependencies or building project…'
                sh 'ls -la'
            }
        }

        stage('Test') {
            steps {
                echo 'Running Tests…'
                // sh 'npm test' or whatever your project's test command is
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying…'
                // sh 'deployment command'
            }
        }
    }
}
