#!/usr/bin/env groovy

pipeline
{

	agent { label 'docker' }

	stages{
	
		stage('build') 
			{
			steps{

   	  			sh 'sudo docker build --pull=true -t ec2-34-213-54-39.us-west-2.compute.amazonaws.com/hello-jenkins:$GIT_COMMIT .'

				} 
			}

		stage('test')
			{
			steps{
				sh 'sudo docker run -i --rm ec2-34-213-54-39.us-west-2.compute.amazonaws.com/hello-jenkins:$GIT_COMMIT ./script/test' 
				}
			}	


		}
}