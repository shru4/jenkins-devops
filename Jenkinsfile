pipeline {
	agent any
	environment {
		//dockerHome = tool 'myDocker'
		mavenHome = tool 'myMaven'
		PATH = "$mavenHome/bin:$PATH"
	}
	//agent { docker { image 'node:13.8'} }
	stages {
		stage('Build') {
			steps {
				sh 'mvn --version'
				echo "Build"
				echo "PATH - $PATH"
				echo "BUILD_NUMBER - $env.BUILD_NUMBER"
				echo "BUILD_ID - $env.BUILD_ID"
				echo "JOB_NAME - $env.JOB_NAME"
				echo "BUILD_TAG - $env.BUILD_TAG"
				echo "BUILD_URL - $env.BUILD_URL"
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
			echo "Always"
		}
		success {
			echo "Success"
		}
		failure {
			echo "Failure"
		}
	}
}
