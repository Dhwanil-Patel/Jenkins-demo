pipeline {
	agent any
	stages {
		stage ("Resource CLeanuo") {
			steps {
				deleteDir()
			}
		}
		stage ("Clone") {
			steps {
				git url:"https://github.com/Dhwanil-Patel/Jenkins-demo.git", branch:"develop"
			}
		}
		stage ("Build") {
			steps {
				dir("Jenkins-demo-service") {
					sh "mvn clean install"
				}
			}
		}
		stage ("Test") {
			steps {
				dir("Jenkins-demo-service") {
					sh "mvn test"
				}
			}
		}
		stage ("Complete") {
			steps {
				echo "Execution completed"
			}
		}
	}
}