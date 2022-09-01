pipeline {
    agent none
    stages {
        stage('Typescript') {
            agent {
                docker {
                    image 'node:17-bullseye'
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