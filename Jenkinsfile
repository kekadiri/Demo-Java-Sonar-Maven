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
                    sh 'mvn deploy'
                    nexusArtifactUploader credentialsId: 'nexus', groupId: 'pom.org.sonarqube', nexusUrl: '18.215.156.65:8081/', nexusVersion: 'nexus3', protocol: 'http', repository: 'maven-releases', version: 'pom.1.0-SNAPSHOT'
                }
            }
        
        }
}
