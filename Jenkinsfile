pipeline {
    agent {
        docker { image 'node:20.11.0-alpine3.19' }
    }

    stages {
        stage('Lint') {
            steps {
                // Clone the repository
                checkout scm

                // Run linting
                dir('nextjs-app') {
                    sh 'npm install'
                    sh 'npm run lint'
                }
            }
        }

        stage('Build') {
            steps {
                // Run build
                dir('nextjs-app') {
                    sh 'npm run build'
                }
            }
        }
    }
}
