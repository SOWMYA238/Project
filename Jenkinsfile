pipeline{
	agent {label 'master'}
	tools{ maven 'M3'}

		stage('Build') {
			steps {
				sh 'mvn clean compile'
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

