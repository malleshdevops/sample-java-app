pipeline {
    agent any
    options { buildDiscarder(logRotator(numToKeepStr: '10')) }
    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "maven"
    }

    stages {
        stage('Build') {
            steps {
                // Get some code from a GitHub repository
                // git branch: 'main', url: 'https://github.com/malleshdevops/sample-java-app.git'

                // Run Maven on a Unix agent.
                sh "mvn -Dmaven.test.failure.ignore=true clean package"

                // To run Maven on a Windows agent, use
                // bat "mvn -Dmaven.test.failure.ignore=true clean package"
            }
        }
    }
}
