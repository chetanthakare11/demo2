pipeline {
	agent any
	
	stages {
		stage ('Compile Stage') {
			
			steps {
				withMaven(maven : 'my_maven') {
				sh 'mvn clean compile'
				}
			}
		}
		stage ('Testing Stage') {
			steps {
				withMaven(maven : 'my_maven') {
				sh 'mvn test'
				}
			}
		}
		stage ('Packaging Stage') {
			steps {
				withMaven(maven : 'my_maven') {
				sh 'mvn package'
				}
			}
		}
	}
}
