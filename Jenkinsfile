node {
	def app
	
	stage('Clone repository') {
		checkout scm
	}

	stage('Build image') {
		app = docker.build('francotian/example-app')		

	}

	stage ('Push image'){
		docker.withRegistry('https://registry.example.com', 'docker-cred') {
			app.push('latest')

		}	

	}
}
