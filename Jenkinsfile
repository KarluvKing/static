pipeline {
	agent any
	stages {
		stage('Upload to AWS') {
			steps {
				sh 'echo "aqui 01"'
				withAWS(credentials:'4bb02980-af4c-4773-98a4-9e9979ad1f17', region:'us-east-2') {
					sh 'echo "aqui 02"'
					s3Upload(file:'index.html', bucket:'jenkinswebsite1900')
				}
			}
		}
	}
}
