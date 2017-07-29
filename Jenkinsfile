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
				sh 'printenv'
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