pipeline {
    agent none
    stages {
        stage('Waiting 1') {
            agent {
                node {
                    label 'maven'
                }
            }
            steps {
                script {
                // This step pauses Pipeline execution and allows the user to interact and control the flow of the build.
                // Only a basic "process" or "abort" option is provided in the stage view
                input message: '', ok: 'Proceed',
                        parameters: [
                                string(name: '', description: ''),
                        ]
                }
            }
        }

        stage('Maven version') {
            agent {
                node {
                    label 'maven'
                }
            }
            steps {
                echo "Hello, Maven"
                sh "mvn --version" // Runs a Bourne shell script, typically on a Unix node
            }
        }

        stage('Waiting 2') {
            agent {
                node {
                    label 'nodejs'
                }
            }
            steps {
                script {
                // This step pauses Pipeline execution and allows the user to interact and control the flow of the build.
                // Only a basic "process" or "abort" option is provided in the stage view
                input message: '', ok: 'Proceed',
                        parameters: [
                                string(name: '', description: ''),
                        ]
                }
            }
        }

        stage('NodeJS version') {
            agent {
                node {
                    label 'nodejs'
                }
            }
            steps {
                echo "Hello, NodeJS"
                sh "node --version" // Runs a Bourne shell script, typically on a Unix node
            }
        }
    }
}