pipeline {
	agent any 
		stages {
		stage('git repo & clean') {
		steps {
			sh "rm -rf TheSportyShop"
			sh "git clone https://github.com/paulmifsud636/TheSportyShop.git" 
			sh "mvn clean -f TheSportyShop"
			}
		}
		stage('install') {
			steps {f
				sh "mvn install -f TheSportyShop"
			}
		}
		stage('test'){
			steps {
				sh "mvn test -f TheSportyShop"
			}
		}
		stage('pakage'){
			steps {
				sh "mvn package -f TheSportyShop"
			}
		}
	}
}