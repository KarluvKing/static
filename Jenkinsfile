    
pipeline {
	agent any
	stages {
		stage('Build') {
			steps {
				withAWS(profile:'myProfile') {
					s3Upload(file:'index.html', bucket:'jenkinswebsite1900', path:'/')
				}
			}
		}
	}
}
