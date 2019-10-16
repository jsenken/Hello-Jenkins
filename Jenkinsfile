pipeline {
    agent any

    stages {

        stage('build') {
            steps {
                    sh 'cd ..'
                    sh 'pwd'
                    sh 'chmod 777 rsvp-service'
                    sh 'cd rsvp-service'
                    sh 'pwd'
                dir("${env.WORKSPACE}/rsvp-service"){
                    
                        
                    // sh 'cd ./rsvp-service'
                    sh 'sudo ./mvnw -DskipTests clean compile' 
                }
            }
        }

        stage('test') {
            steps {
                    sh 'cd ..'
                    sh 'pwd'
                    sh 'chmod 777 rsvp-service'
                    sh 'cd rsvp-service'
                    sh 'pwd'
              dir("${env.WORKSPACE}/rsvp-service"){
                    
                    // sh 'cd rsvp-service'
                    sh 'sudo ./mvnw test' 
              }
            }
        }

        stage('deliver') {
            steps {
                sh 'cd ..'
                    sh 'pwd'
                    sh 'chmod 777 rsvp-service'
                    sh 'cd rsvp-service'
                    sh 'pwd'
              dir("${env.WORKSPACE}/rsvp-service"){
                    
                    // sh 'cd rsvp-service'
                    sh 'sudo ./mvnw -DskipTests install' 
              }
            }
        }

    }
}
