#!/usr/bin/env groovy

pipeline
{
	properties([pipelineTriggers([githubPush()])])

node {
    git url: 'https://github.com/afiffing/hello-jenkins.git', branch: 'master'
}


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