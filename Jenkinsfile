pipeline{
  agent any
  stages{
  	stage('version-control'){
  		steps{
  			git checkout
  		}
  	}
  	stage ('parallel-job1'){
  		parallel{
  		  stage ('sub-job1'){
  		  	steps{
  		  	  echo 'action1'
  		  	}
  		  }
  		  stage ('sub-job2'){
  		  	steps{
  		      echo 'action2'  	
  		  	}
  		  }
			stage('sub-job3'){
				steps{
					echo 'action3'
				}
			}
  		}
  	}
  	stage ('code build'){
  		steps{
  			sh 'cat/etc/passwd'
  		}
  	}
  }
}