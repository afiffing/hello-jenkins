#!/usr/bin/env groovy

pipeline
{
	
	agent { label 'docker' }
	properties([buildDiscarder(logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '', daysToKeepStr: '15', numToKeepStr: '2')), pipelineTriggers([githubPush()])])

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