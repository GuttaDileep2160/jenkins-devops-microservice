pipeline {
    agent any

	environment{
		dockerHome = tool 'myDocker'
		mavenHome = tool 'myMaven'
		PATH = "$dockerHome\bin:$mavenHome\bin:$PATH"
	}

	//agent { docker { image  'maven:3.8.6'  } }
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
				sh 'docker --version'
				echo "PATH - $PATH"
				echo "BuildNumber - $env.BUILD_NUMBER"
				echo "BUILDTAG - $env.BUILD_TAG"
				echo "BUILDid - $env.BUILD_ID"
				echo "BUILDURL - $env.BUILD_URL"
				echo "JOBNAME - $env.JOB_NAME"
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