#!/usr/bin/env groovy

pipeline
{

	agent { label 'docker' }

	 environment {
	 filepath = '/home/ubuntu/abc'
	 }

	stages{
	
		stage('dev') 
			{
			steps{
   	  			sh 'cat filepath'
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