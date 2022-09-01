pipeline {
    agent none
    stages {
        stage('Typescript') {
            agent {
                docker {
                    image 'node:16-alpine'
                }
            }
            stages {
                stage('Typescript Build') {
                    steps {
                        dir('DotnetTemplate.Web/') {
                            sh 'npm ci'
                            sh 'npm run build'
                        }
                    }
                }
            }
        }
    }
}