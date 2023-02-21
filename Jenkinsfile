pipeline {
	agent any
	stages {
	    stage ('clean up') {
	        steps {
	            cleanWs()
	        }
			}
		stage ('build') {
			steps {
			    dir ('Git-Project1'){
				    echo "Hello Sunil again!!"
				    sh 'mvn clean install -DskipTests'
			    }
			}
		
		}
		stage ('test') {
			steps {
			    dir ('Git-Project1') {
				    sh 'mvn test'
			    }
      }
    }
  }
}

