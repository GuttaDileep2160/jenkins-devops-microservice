pipeline {
    //agent any

	agent { image { 'maven:3.8.6' } }
    stages {
        stage('Hello') {
            steps {
                echo 'Hello welcome to Jenkins'
            }
        }
        stage('Build') {
            steps {
                echo 'Bulilding the project'
				echo 'mvn --version'
				sh 'mvn --version'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing the project'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying the project'
            }
        }
        stage('Release') {
            steps {
                echo 'Releasig the project'
            }
        }
    }

	post{
		always{
			echo 'i will run always'
		}
		success {
			echo 'i run only during success'
		}
		failure{
			echo 'i run only during failure'
		}
	}
}