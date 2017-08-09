#!/usr/bin/env groovy

pipeline
{

	agent { label 'docker' }

	stages{
	
		stage('build') 
			{
			steps{

   	  			sh 'sudo docker build --pull=true -t hello-jenkins:$GIT_COMMIT .'

				} 
			}

		stage('test')
			{
			steps{
				sh 'sudo docker run -i --rm hello-jenkins:$GIT_COMMIT ./script/test' 
				}
			}	


		}
}