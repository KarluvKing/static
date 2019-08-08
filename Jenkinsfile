pipeline {
	agent any
	stages {
		stage('Upload to AWS') {
			steps {
				withAWS(credentials:'4bb02980-af4c-4773-98a4-9e9979ad1f17', region:'us-east-2') {
					s3Upload(file:'index.html', bucket:'jenkinswebsite1900')
					sh 'echo "Completed with success"'
				}
			}
		}
	}
}
