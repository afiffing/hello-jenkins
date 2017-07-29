#!/usr/bin/env groovy

pipeline
{

	agent { label 'docker' }

	 parameters { string(name: 'filepath', defaultValue: '/home/ubuntu/abc', description: 'yo! you got it.') }

	stages{
	
		stage('dev') 
			{
			steps{
   	  			sh 'cat ${params.filepath}'
				} 
			}

		stage('qa')
			{
			steps{
				sh 'ls -al ${params.filepath}'
				}
			}	


		}
}