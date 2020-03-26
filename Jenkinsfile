currentBuild.displayName = "Reliance_Harikrishna_#"+currentBuild.number
pipeline{
	agent any
	
	options {
		buildDiscarder logRotator(daysToKeepStr: '5', numToKeepStr: '7')
	}
	environment {
		PATH = "${PATH}:/home/jenkins/maven3/bin"
		
	}
    stages{
      stage('SCM'){
        steps{
          git credentialsId: 'git_credentials', url: 'https://github.com/harikrishna12334/DockerWebApp.git' 
        }
      }
	stage('Maven Build - Clean'){
		steps{
			sh "${PATH}mvn clean"
		}
	}
	stage('Maven Build - compile'){
		steps{
			sh "./mvn compile"
		}
	}
	stage('Maven Build - Test'){
		steps{
			sh "./mvn test"
		}
	}
	    
	    
	    
	    
	    
	    
	    
    }
}
  
