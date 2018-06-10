node('maven') {

    stage('Checkout source code') {
        echo 'Checkout scm'
        checkout scm
    }


    stage('Compile') {
        echo 'Maven compile'
        mvn compile
    }
}