pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'maven_3.5.2') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'maven_3.5.2') {
                    sh 'mvn test'
                }
            }
                stage ('Performance Testing Stage') {

                    steps {
                         echo 'Performance testing'
                         }
                 }
        }


        stage ('Deployment Stage') {
            steps {
                withMaven(maven : 'maven_3.5.2') {
                    sh 'mvn clean install'
                }
            }
        }
    }
}
