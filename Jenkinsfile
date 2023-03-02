pipeline {
	agent {
		label {
			label "built-in"
		}
	}
        tools {
                jdk "java-8"
                maven "maven-3.9"
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
                                    '''
			}
		}
	}
}
