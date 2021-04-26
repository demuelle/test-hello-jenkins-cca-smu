pipeline {
    agent any

    stages {

        stage('build') {
            steps {
              bat '''
                 cd rsvp-service
                 ./mvnw -DskipTests clean compile
              '''
            }
        }

        stage('test') {
            steps {
              bat '''
                 cd rsvp-service
                     ./mvnw test
              '''
            }
        }

        stage('deliver') {
            steps {
              bat '''
                 cd rsvp-service
                     ./mvnw -DskipTests install
              '''
            }
        }

    }
}