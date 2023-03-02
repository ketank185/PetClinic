pipeline {
	agent {
		label {
			label "built-in"
		}
	}
	stages {
		stage ("clean workspace") {
			steps {
				cleanWs ()
			}
		}
		stage ("checkout from SCM") {
			steps {
				checkout scm
			}
		}
		stage ("building project") {
			steps {
				sh ''' 
					mvn clean
					mvn package
			}
		}
	}
}
