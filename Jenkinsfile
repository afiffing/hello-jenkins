#!/usr/bin/env groovy

pipeline
{

	agent { label 'docker' }

	stages{
	
		stage('dev') 
			{
			properties([buildDiscarder(logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '', daysToKeepStr: '15', numToKeepStr: '7')), [$class: 'GithubProjectProperty', displayName: '', projectUrlStr: 'https://github.com/afiffing/hello-jenkins.git/'], pipelineTriggers([githubPush()])])

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