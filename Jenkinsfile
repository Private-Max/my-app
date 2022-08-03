pipeline {
    agent any 
    stages {
        stage('fetch code') {
            steps {
                git 'https://github.com/Private-Max/my-app.git'
            }
        }
        stage('build package') {
            steps {
                sh 'mvn clean package'
            }
        }
        stage('SonarQube Analysis') {
            steps {
               sh '${mvn}/bin/mvn clean verify sonar:sonar -Dsonar.projectKey=sonar-prj-1 -Dsonar.host.url=http://34.228.20.228:9000'
				}
			}
		}
	}
