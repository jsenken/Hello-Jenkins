pipeline {
    agent any

    stages {

        stage('build') {
            steps {
                dir("${env.WORKSPACE}/rsvp-service"){
                    sh 'chmod 777 ./rsvp-service'
                    sh 'pwd'
                        
                    // sh 'cd ./rsvp-service'
                    sh './mvnw -DskipTests clean compile' 
                }
            }
        }

        stage('test') {
            steps {
              dir("${env.WORKSPACE}/rsvp-service"){
                    sh 'chmod 777 ./rsvp-service'
                    sh 'pwd'
                    // sh 'cd rsvp-service'
                    sh './mvnw test' 
              }
            }
        }

        stage('deliver') {
            steps {
              dir("${env.WORKSPACE}/rsvp-service"){
                    sh 'chmod 777 ./rsvp-service'
                    sh 'pwd'
                    // sh 'cd rsvp-service'
                    sh './mvnw -DskipTests install' 
              }
            }
        }

    }
}
