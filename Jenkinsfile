pipeline {
    agent any
        stages {
            stage('build') {
                steps {
                    sh 'mvn package'
                }
            }
            stage('sonar') {
                steps {
                   sh 'mvn sonar:sonar'
                }    
            
            }
        }
}
