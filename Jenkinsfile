pipeline {
  agent {
    label 'masternode'
  }
  parameters {
    string defaultValue: 'prod', description: 'prod|stg|dev', name: 'environmental'
  }
  stages {
    stage('GIT-CLONE') {
      steps {
      git credentialsId: 'mydeploy', url: 'https://github.com/saravananajay/JenkinsWar.git' 
      }
    }
    stage('MAVEN-BUILD') {
      steps {
      sh  """
	   
	  /opt/maven/bin/mvn clean install 
	   
	  """
      }
    }	
  }
}
