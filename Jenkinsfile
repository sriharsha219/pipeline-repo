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
                        not {
                                branch 'master'
                        }
                }
                steps {
			echo 'this is from stage-Three'
                        }
        }

    }
}

