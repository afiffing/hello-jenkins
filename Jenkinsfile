#!/usr/bin/env groovy

pipeline
{
	options([[$class: 'GithubProjectProperty', displayName: '', projectUrlStr: 'https://github.com/afiffing/hello-jenkins.git/'], pipelineTriggers([githubPush()])])


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