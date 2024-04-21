pipeline {
    agent { node { label 'AGENT' } }
    stages {      
        stage('Install depdencies') {
            steps {
                sh 'ls -ltr'
                sh 'pwd'
                sh 'npm install'
            }
        }
        stage('Unit test') {
            steps {
                echo "unit testing is done here"
            }
        }
        //sonar-scanner command expect sonar-project.properties should be available
        stage('Sonar Scan') {
            steps {
                echo "Sonar scan done"
                sh '''
                ls -ltr
                sonar-scanner
                '''
            }
        }

    }


}