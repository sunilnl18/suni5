pipeline {
	agent any
	stages {
	    stage ('clean up') {
	        steps {
	            cleanWs()
	        }
	    }
	    
	    stage ('clone') {
			steps {
				sh 'git clone https://github.com/sunilnl18/suni5.git'
			}
	    }
		stage ('build') {
			steps {
			    dir ('suni5'){
				    echo "Hello Sunil again!!"
				    sh 'mvn clean install -DskipTests'
			    }
			}
		
		}
		stage ('test') {
			steps {
			    dir ('suni5') {
				    sh 'mvn test'
			    }
      }
    }
  }
}
