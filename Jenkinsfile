pipeline {

    agent any

     def tomcatWeb = '/home/dineshreddy99077/noida/apache-tomcat-7.0.103/webapps'
     def tomcatWeb = '/home/dineshreddy99077/noida/apache-tomcat-7.0.103/bin'
     def tomcatStatus = ''
    stages {

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
         
         stage('deploy in tomcat')
          sh "cp target

        

    }

}

