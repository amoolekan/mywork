pipeline {
    agent any
    
    tools {
        maven 'MVN'
    }
stages{
        stage('Build'){
            steps {
                sh 'mvn clean package'
            }
            post {
                success {
                    echo 'Archiving the artifacts 2'
                    archiveArtifacts artifacts: '**/target/*.war'
                }
            }
        }

        stage ('Deployments'){
            parallel{
                stage ("Deploy to Staging"){
                    steps {
                        
                    }
                }
            }
        }
    }
}