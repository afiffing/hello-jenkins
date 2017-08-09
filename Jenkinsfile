#!/usr/bin/env groovy

pipeline
{
	git([url: 'https://github.com/afiffing/hello-jenkins.git', branch: 'master'])

	agent { label 'docker' }

	options { [buildDiscarder(logRotator(numToKeepStr: '2'), pipelineTriggers([githubPush()]))] }

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