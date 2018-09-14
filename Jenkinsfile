pipeline {
    agent {
        docker {
            image 'node:6-alpine' 
            args '-p 3000:3000' 
        }
    }
    environment {
	CI = 'true'
    }
    stages {
        stage('Build') { 
            steps {
                sh 'npm install' 
            }
        }
	stage('Test') {
		steps {
			sh '/home/Sites/simple-node-js-react-npm-app/jenkins/script/test.sh'
		}
	}
    }
}
