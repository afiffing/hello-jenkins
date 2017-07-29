#!/usr/bin/env groovy

pipeline
{
	agent { label 'docker' }

	stages{
	
		stage('dev') 
			{
			steps{
   	  			sh 'cat /home/ubuntu/abc'
				} 
			}

		stage('qa')
			{
			steps{
				sh 'ls -al /home/ubuntu/abc'
				}
			}	


		}
}