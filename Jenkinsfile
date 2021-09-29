pipeline {
	agent any
	
	stages {
		stage("build") {

			steps {
				sh 'make'
				echo "building the application..."	
			}
		}
		
		stage("test") {
			steps {
				echo "testing the application..."
			}
		}

		stage("deploy") {
			when {
				expression {
					BRANCH_NAME == 'main'
				}
			}
			steps {
				echo "deploying the application..."
			}
		}
	}
}
