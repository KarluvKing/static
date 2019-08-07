    
pipeline {
	agent any
	stages {
		stage('Build') {
			steps {
				withAWS(profile:'myProfile') {
					s3Upload(file:'file.txt', bucket:'my-bucket', path:'path/to/target/file.txt')
				}
			}
		}
	}
}
