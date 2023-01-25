pipeline {
    agent { label 'swarm' }
    stages {
        stage('Clone Down') {
            steps {
                stash exclude: '.git/**', name: 'code'
            }
        }
        stage('Build App') {
            options { skipDefaultCheckout(true) }
            steps {
                unstash 'code'
            }
        }
    }
}
