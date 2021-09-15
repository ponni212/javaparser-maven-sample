pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'maven_3_8_2') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'maven_3_8_2') {
                    sh 'mvn test'
                }
            }
        }

         stage ('build stage') {
              
            steps {
                withMaven(maven: 'maven_3_8_2') {
                    sh 'maven build'
                }
            }
        }

        stage ('Deployment Stage') {
            steps {
                withMaven(maven : 'maven_3_8_2') {
                    sh 'mvn deploy'
                }
            }
        }
    }
}