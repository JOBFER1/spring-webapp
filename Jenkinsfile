pipeline {
  agent any
  
  tools {
    maven 'Maven 3.8.6' 
  }

  stages {
    stage ('Build') {
      steps {
        bat 'mvn clean package'
      }
    }
    

    stage ('Deploy') {
    	steps {
	    	//bat "move target/webapptest.war C:/apache-tomcat-10.0.27/webapps"
	    	bat "powershell Copy-Item target/webapptest.war -Destination C:/apache-tomcat-10.0.27/webapps"
	  	}
	}

  }
}