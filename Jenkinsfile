//DECLARATIVE format
pipeline {
	agent { 
		docker { 
			image 'maven:3.6.3'
			label 'docker'
		}
	}
	stages {
		stage('Build') {
			steps {
				sh "mvm --version"
				echo "Build"
			}
		}
		stage('Test') {
			steps {
				echo "Test"
			}
		}
		stage('Integration Test') {
			steps {
				echo "Integration Test"
			}
		}
	}

    post {
	    always {
			echo 'Im awedome. I run always'
		}
		success {
			echo 'I run when you are successful'
		}
		failure {
			echo 'I run when you ar fail'
			
		}
	}
}





/*scripted new one
node{
	echo "Build"
	echo "Test"
	echo "Integration Test"
}





node {
	stage('Build') {
		echo "Build"
	}
	stage('Test') {
		echo "Test"
	}
	stage('Integration Test') {
		echo "Test"
	}
}*/
