pipeline {
	agent any
	stages {
		stage('Upload to AWS') {
			steps {
				//withAWS(credentials:'IDofSystemCredentials', region:'eu-west-2') {
				//	s3Upload(file:'index.html', bucket:'jenkinswebsite1900', path:'/')
				//}
				
				withCredentials([[$class: 'AmazonWebServicesCredentialsBinding', accessKeyVariable: 'AWS_ACCESS_KEY_ID', credentialsId: '', secretKeyVariable: 'AWS_SECRET_ACCESS_KEY']]) {
					s3Upload(file:'index.html', bucket:'jenkinswebsite1900', path:'/')
				}
				
				sh 'echo "Hello World"'
				sh '''
					echo "Multiline shell steps works too"
					ls -lah
				'''
				}
			}
		}
	}


//pipeline {
//	agent any
//	stages {
//		stage('Upload to AWS') {
//			steps {
//				withCredentials([[$class: 'AmazonWebServicesCredentialsBinding', accessKeyVariable: 'AWS_ACCESS_KEY_ID', credentialsId: '', secretKeyVariable: 'AWS_SECRET_ACCESS_KEY']]) {
//					s3Upload(file:'index.html', bucket:'jenkinswebsite1900', path:'/')
//				}
//			}
//		}
//	}
//}
