pipeline {
    agent any
    stages {
        stage('scanes') {
            parallel {
                stage('sonar') {
                    steps {
                        echo "sonar is executing"
                        sleep 10
                    }
                }stage ('DeployToProd'){
                    options{
                        timeout(time:300, unit:'SECONDS')
                    }input message: "Doing Prod Deployment", ok:'yes', submittes: 'dev-lahari','test-ani'
                }
                    }
                }
            } // closes parallel
        } // closes 'scanes' stageloses pipeline
