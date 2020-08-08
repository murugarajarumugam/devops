pipeline {
    agent none

    stages {
        stage('Code') {
	agent {label 'master'}
            steps {
                build job:  'Code'
		echo "Coding"
            }
        }
      
	stage('Build') {
        agent {label 'master'}
	    steps {
                build job:  'Build'
		echo "Building"
            }
        }

	stage('Test') {
	agent {label 'master'}
            steps {
                build job:  'Test'
		echo "Testing"
            }
        }

	stage('Deploy') {
	agent {label 'master'}
            steps {
                build job:  'Deployment'
		echo "Deploying"
            }
        }

    }

}