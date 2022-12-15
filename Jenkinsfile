node {
	def app
	
	stage('Clone repository') {
		checkout scm
	}

	stage('Build image') {
		app = docker.build('francotian/example-app')		

	}

	stage ('Push image'){
		withRegistry([ credentialsId: "docker-cred", url: "" ]){
			app.push('latest')

		}	

	}
}
