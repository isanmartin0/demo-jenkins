pipeline {
    agent {
        node {
            label 'my-defined-label'
            customWorkspace '/some/other/path'
        }
    }
    stages {
        stage('Example') {
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
            steps {
                echo "Hello, Maven"
                sh "mvn --version" // Runs a Bourne shell script, typically on a Unix node
            }
        }
    }
}