pipeline {
    agent any

    stages {

        stage('build') {
            steps {
              sh '''
                 chmod 777 rsvp-service
                 cd ./rsvp-service
                 ./mvnw -DskipTests clean compile
              '''
            }
        }

        stage('test') {
            steps {
              sh '''
                 chmod 777 rsvp-service
                 cd rsvp-service
                     ./mvnw test
              '''
            }
        }

        stage('deliver') {
            steps {
              sh '''
                 chmod 777 rsvp-service
                 cd rsvp-service
                     ./mvnw -DskipTests install
              '''
            }
        }

    }
}
