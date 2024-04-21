pipeline {
    agent none
    stages {
        stage('Maven Install') {
            agent {
                docker {
                    image 'maven:3.5.0'
                }
            }
            steps {
                sh 'mvn clean install'
            }
            steps {
                script {
                    docker.image('maven:3.5.0').pull()
                }
            }
        }
    }
}
