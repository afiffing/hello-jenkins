#!/usr/bin/env groovy

pipeline
{

	agent { label 'docker' }

	stages{
	
		stage('build') 
			{
			steps{
				sh "git rev-parse --short HEAD > /home/ubuntu/commit-id"                        
				commit_id = readFile('/home/ubuntu/commit-id')
   	  			sh 'sudo docker build --pull=true -t hello-jenkins:$commit_id .'
				} 
			}

		stage('test')
			{
			steps{

				gitCommit = sh(returnStdout: true, script: 'git rev-parse HEAD').trim()

				sh 'sudo docker run -i --rm hello-jenkins:$gitCommit ./script/test' 
				}
			}	


		}
}