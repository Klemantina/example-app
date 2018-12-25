node {
	def app
	
	stage('Clone repository') {
		checkout scm
	}

	stage('Build image') {
		app = docker.build('klemantina/example-app')
	}

	stage('Push image') {
		docker.withRegistry('https://registry.hub.docker.com', 'docker-hub') {
			app.push('latest')

		}
	}


}
