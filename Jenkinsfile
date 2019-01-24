pipeline {
    agent { label 'docker-agent' }

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
		sh 'pwd'
		sh 'ls -l'
		sh 'go version'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
