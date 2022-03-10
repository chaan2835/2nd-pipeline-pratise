pipeline {
    agent any
    stages {
        stage('Example Build') {
            agent { label "slave-node" }
            steps {
                sh 'echo Hello World'
            }
        }
        stage('Ready to Deploy') {
             	    agent {label "slave-node-2"}
	    steps {
                input(message: "Deploy to production?")
            }
        }
        stage('Example Deploy') {
            agent { label "slave-node "}
            steps {
                sh 'echo Deploying'
            }
        }
    }
}
