node {
	def app
	
	stage('Clone repository') {
		checkout scm
	}

	stage('Build image') {
		app = docker.build('tianco/example-app')		

	}

	stage ('Push image'){
		docker.withRegistry('https://registry.hub.docker.com', 'docker-cred') {
			app.push('latest')

		}	

	}
}
