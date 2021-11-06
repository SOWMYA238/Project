pipeline{
	agent {label 'master'}
	tools{ maven 'M3'}
	stages {

		stage('Build') {
			steps {
				sh 'javac DigitalBankApplication.java'
			}
		}
		stage('Test') {
			steps {
				sh 'mvn test'
			}
		}
                stage('Package') {
			steps {
				sh 'mvn package'
                                archiveArtifacts artifacts: 'target/*.jar', followSymlinks: false
			}
		}
	}
				
	}

