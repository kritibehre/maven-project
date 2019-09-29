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
	    
	    stage ('deploy to tomcat') {


steps {
  sshagent (['18.222.20.202']) {
    sh 'scp -o StrictHostKeyChecking=no **/*.war ec2-user@18.222.20.202:/var/lib/tomcat/webapps'
      }
}
}
		}
		}
		
