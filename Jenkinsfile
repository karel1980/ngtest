pipeline {
	agent {
        docker { 
        	image 'node:10-alpine' 
        	args '-u 1000:1000'
        }
    }
	stages {
		stage('Install') {
			steps {
				sh 'echo $HOME'
				sh 'whoami'
				sh 'npm install && npm rebuild'
			}
		}
		stage('Build') {
			steps {
				sh 'npm run test:headless'
			}
		}
	}
}

