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
  		}
  	}
  	stage ('code build'){
  		steps{
  			sh 'cat/etc/passwd'
  		}
  	}
  }
}