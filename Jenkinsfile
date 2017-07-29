#!/usr/bin/env groovy

pipeline
{
	agent { label 'docker' }

	stages{
	
		stage('dev') 
			{
   	  		sh 'cat /home/ubuntu/abc'
			}

		stage('qa')
			{

			sh 'ls -al /home/ubuntu/abc'

			}	


		}
}