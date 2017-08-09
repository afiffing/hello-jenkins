#!/usr/bin/env groovy

pipeline
{

	agent { label 'docker' }

	stages{
	
		stage('build') 
			{
			steps{
				gitCommit = sh(returnStdout: true, script: 'git rev-parse HEAD').trim()

   	  			sh 'sudo docker build --pull=true -t hello-jenkins:$gitCommit .'

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