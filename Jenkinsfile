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
           // sh 'AWS_ACCESS_KEY_ID=AKIA5YLD7IJGMGBIOY6P AWS_SECRET_ACCESS_KEY=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 aws s3 cp index.html s3://my-datastorage'//
		 withCredentials([<object of type com.cloudbees.jenkins.plugins.awscredentials.AmazonWebServicesCredentialsBinding>]) {
			 sh 'aws s3 cp index.html s3://my-datastorage'
			 }
         }
	}
   }
}
