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
        stage('Push') {
            steps {
                echo 'Pushing..'
                sh 'docker tag hello-world:jenkins-${BUILD_NUMBER} iad.ocir.io/davin2019/travel-agency-front/hello-world:${BUILD_NUMBER}'
                sh 'docker push iad.ocir.io/davin2019/travel-agency-front/hello-world:${BUILD_NUMBER}'
            }
        }
    }
}
