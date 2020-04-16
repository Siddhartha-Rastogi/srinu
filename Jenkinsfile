pipeline {

    agent any

     
    stages {
        
        stage ('checkout'){
            steps {
            git  'https://github.com/dinrag/srinu.git'
            }
        }

        stage ('compile') {

            steps {

                withMaven(maven : '/opt/mvn/apache-maven-3.6.3') {

                    sh 'mvn clean compile'

                }

            }

        }

    



        stage ('test') {

            steps {

                withMaven(maven : '/opt/mvn/apache-maven-3.6.3') {

                    sh 'mvn test'

                }

            }

        }

        

        

        stage ('package') {

            steps {

                withMaven(maven : '/opt/mvn/apache-maven-3.6.3') {

                    sh 'mvn package'
                   

                }

            }

         }
        
        stage ('deploy') {
            
           sh 'cp target/TomcatMavenApp-2.0.war /home/dineshreddy99077/noida/apache-tomcat-7.0.103/webapps/'
     
        }

    }

