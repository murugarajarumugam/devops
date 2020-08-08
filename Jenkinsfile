pipeline {
    agent none

    stages {
        stage('Code') {
	agent {label 'centos'}
            steps {
                build job:  'Code'
		echo "Coding"
            }
        }
      
	stage('Build') {
        agent {label 'centos'}
	    steps {
                build job:  'Build'
		echo "Building"
            }
        }

	stage('Test') {
	agent {label 'centos'}
            steps {
                build job:  'Test'
		echo "Testing"
            }
        }

	stage('Deploy') {
	agent {label 'centos'}
            steps {
                build job:  'Deployment'
		echo "Deploying"
            }
        }

    }

}