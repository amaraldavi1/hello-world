pipeline {
    agent any
    tools {
        maven 'Maven3'
    }
    stages {
        stage ('Sonar') {
            steps {
                sh '''
                  mvn clean verify sonar:sonar 
		  -Dsonar.projectKey=test-Project \
		  -Dsonar.host.url=http://localhost:9000 \
		  -Dsonar.login=dcdd54218f0cb93039b54091fd293021afb41d6c

		'''
            }
        }

        }
    }
}
