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
				}
	}
