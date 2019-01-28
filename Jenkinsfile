pipeline {
    agent { label 'docker-agent' }

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
		sh 'pwd'
		sh 'docker build -t hello-world:jenkins-${BUILD_NUMBER} .'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
		sh 'docker images | grep hello-world'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
