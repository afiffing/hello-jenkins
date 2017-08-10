#!/usr/bin/env groovy

pipeline
{

	agent { label 'docker' }

	stages{
	
		stage('build') 
			{
			steps{
   	  			sh 'sudo docker build --pull=true -t hello-jenkins .'
				} 
			}

		stage('test')
			{
			steps{
				sh 'sudo docker run -i --rm hello-jenkins ./script/test' 
				}
			}	


		}
}