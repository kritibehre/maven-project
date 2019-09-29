pipeline {
    agent any


    stages 
    {  
        
        stage ('SCM Checkout') {
          git 'https://github.com/prakashk0301/maven-project.git'
         }
    
    }
    {
                            
        
        stage ('Testing Stage') {


            steps {
                withMaven(maven : 'LocalMaven')
                {
                    sh 'mvn test'
                }
                  }
                                 
        }
	    
	     stage ('Package Stage') {


            steps {
                withMaven(maven : 'LocalMaven')
                {
                    sh 'mvn Package'
                }
                  }
                                 
        }
	    
	       stage ('install Stage') {


            steps {
                withMaven(maven : 'LocalMaven')
                {
                    sh 'mvn install'
                }
                  }
                                 
        }
	   
		}
		
