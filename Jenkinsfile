pipeline {
    agent any

    stages {
        stage('Code') {
            steps {
                build job:  'Code'
		echo "Coding"
            }
        }
      
	stage('Build') {
            steps {
                build job:  'Build'
		echo "Building"
            }
        }

	stage('Test') {
            steps {
                build job:  'Test'
		echo "Testing"
            }
        }

	stage('Deploy') {
            steps {
                build job:  'Deployment'
		echo "Deploying"
            }
        }

    }

}