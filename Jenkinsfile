pipeline {
    agent any

    stages {

        stage('build') {
            steps {
                dir("${env.WORKSPACE}/rsvp-service"){
                    sh 'pwd'
                        
             // sh 'cd ./rsvp-service'
                    sh './mvn -DskipTests clean compile' }
            }
        }

        stage('test') {
            steps {
              dir("${env.WORKSPACE}/rsvp-service"){
              sh 'pwd'
              // sh 'cd rsvp-service'
                  sh './mvn test' }
            }
        }

        stage('deliver') {
            steps {
              dir("${env.WORKSPACE}/rsvp-service"){
               sh 'pwd'
              // sh 'cd rsvp-service'
                  sh './mvn -DskipTests install' }
            }
        }

    }
}
