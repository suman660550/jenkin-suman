//DECLARATIVE format
pipeline {
	agent any
	environment {
		dockerHome = tool 'myDocker'
		mavenHome = tool 'myMaven'
		PATH = "dockerHome/bin:$mavenHome/bin:$PATH"
	}
	stages {
		stage('Build') {
			steps {
				//sh 'node --version'
				sh 'mvn --version'
				sh 'docker version'
				echo "Build"
				echo "PATH - $PATH"
				echo "BUILD_NUMBER - $env.BUILD_NUMBER"
				echo "Build_ID - $env.BUILD_ID"
				echo "JOB_NAME - $env.JOB_NAME"
				echo "BUILD_TAG -$env.BUILD_URL"
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
