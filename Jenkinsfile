pipeline
	{
		agent any
			stages
				{
					stage ('scm checkout')
						{
							steps
								{ 
									git branch: 'master', url: 'https://github.com/kritibehre/maven-project.git'

								}
						}
							
					stage ('validate code')
						{
							steps
								{
									withMaven(maven: 'localmaven') 
										{
											sh 'mvn validate'
										}
								}
						}

					stage ('test code')
						{
							steps
								{
									withMaven(maven: 'localmaven') 
										{
											sh 'mvn test'
										}
								}
						}
				}
					
	}
