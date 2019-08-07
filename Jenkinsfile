    
pipeline {
	agent any
	stages {
		stage('Build') {
			steps {
				withCredentials([[$class: 'AmazonWebServicesCredentialsBinding', accessKeyVariable: 'AWS_ACCESS_KEY_ID', credentialsId: '', secretKeyVariable: 'AWS_SECRET_ACCESS_KEY']]) {
					s3Upload(file:'index.html', bucket:'jenkinswebsite1900', path:'/')
				}
			}
		}
	}
}
