pipeline {
	agent any
	stage('Build') {
		echo "Build"
	}
	stage('Test') {
		echo "Test"
	}
	stage('Integration Test') {
		echo "Test"
	}

post{
	always {
		echo 'I always run no matter what'
	}
	success {
		echo 'i run only when all r working fine'
	}
	failure {
		echo 'i run only when something fails'
	}
}
}