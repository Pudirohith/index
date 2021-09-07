pipeline {
   agent any
  stages
   {
   stage('git clone') {
         steps {
            // Get some code from a GitHub repository
            git 'https://github.com/Pudirohith/index.git'
        }  
      }
     stage ('aws-s3') {
         steps {
		 withAWS(credentials:'945639342668') {
           sh 'aws s3 cp index.html s3://my-datastorage'
	 }
         }
	}
   }
}
