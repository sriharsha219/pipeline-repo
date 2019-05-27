pipeline {
    agent any
    stages {
        stage('One') {
                steps {
                        echo 'Hi, this is declarative pipeline demo'
			
                }
        }
	    stage('Two'){
		    
		steps {
			input('Do you want to proceed?')
        }
	    }
        stage('Three') {
                when {
                        expression {
                             sh "git rev-parse --abbrev-ref HEAD > GIT_BRANCH"
                             GIT_BRANCH != 'master'
                     }

                }
                steps {
			sh "mvn install"
                        }
        }

    }
}

