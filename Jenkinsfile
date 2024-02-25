pipeline {
    agent any
        stages {
            stage('build') {
                steps {
                    sh 'mvn package'
                }
            }
            stage('test') {
                steps {
                    echo "testing stage"
                }
            }
            stage('sonar') {
                steps {
                   sh 'mvn sonar:sonar'
                }    
            }
            stage('deploy') {
                steps {
                    echo "depolying"
                }
            }
        
        }
}
