pipeline {
	agent any
	stages {
		stage('Upload to AWS.') {
			steps {
				withAWS(credentials:'IDofSystemCredentials') {
    					s3Upload(file:'index.html', bucket:'jenkinswebsite1900', path:'/')
				}
				//sh 'echo "Hello World"'
				//sh '''
				//	echo "Multiline shell steps works too"
				//	ls -lah
				//'''
				}
			}
		}
	}
