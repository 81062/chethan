pipeline {
    agent any 
    tools {
         maven 'maven'
         jdk 'java'
    }
    stages {

//         stage('Stage-0 : Static Code Analysis Using SonarQube') { 
//             steps {
//                 sh 'mvn clean verify sonar:sonar'
//             }
//         }

        stage('Stage-1 : Clean') { 
            steps {
                sh 'mvn clean'
            }
        }
         stage('Stage-2 : Validate') { 
            steps {
                sh 'mvn validate'
            }
        }
         stage('Stage-3 : Compile') { 
            steps {
                sh 'mvn compile'
            }
        }
         stage('Stage-4 : Test') { 
            steps {
                sh 'mvn test'
            }
        }
          stage('Stage-5 : Install') { 
            steps {
                sh 'mvn install'
            }
        }
          stage('Stage-6 : Verify') { 
            steps {
                sh 'mvn verify'
            }
        }
          stage('Stage-7 : Package') { 
            steps {
                sh 'mvn package'
            }
        }

           stage('Stage-8 : Deploy an Artifact to Artifactory Manager i.e. Nexus/Jfrog') { 
            steps {
                sh 'mvn deploy'
            }
        }

          stage('Stage-9 : Deployment - Deploy a Artifact devops-3.0.0-SNAPSHOT.war file to Tomcat Server') { 
            steps {
                sh 'curl -u admin:redhat@123 -T target/**.war "http://54.199.226.41:8080/manager/text/deploy?path=/chethan&update=true"'
            }
        } 
  
          stage('Stage-10 : SmokeTest') { 
            steps {
                sh 'curl --retry-delay 10 --retry 5 "http://54.199.226.41:8080/chethan"'
            }
        }

  
    }
}








// pipeline {
//     agent any 
//     tools {
//          maven 'maven'
//          java 'java'
//     }
//     stages {

//         stage('Stage-1 : Clean') { 
//             steps {
//                 sh 'mvn clean'
//             }
//         }
//          stage('Stage-2 : Validate') { 
//             steps {
//                 sh 'mvn validate'
//             }
//         }
//          stage('Stage-3 : Compile') { 
//             steps {
//                 sh 'mvn compile'
//             }
//         }
//          stage('Stage-4 : Test') { 
//             steps {
//                 sh 'mvn test'
//             }
//         }
//           stage('Stage-5 : Install') { 
//             steps {
//                 sh 'mvn install'
//             }
//         }
//           stage('Stage-6 : Verify') { 
//             steps {
//                 sh 'mvn verify'
//             }
//         }
//           stage('Stage-7 : Package') { 
//             steps {
//                 sh 'mvn package'
//             }
//         }
//           stage('Stage-8 : Deployment - Deploy a Artifact devops-3.0.0-SNAPSHOT.war file to Tomcat Server') { 
//             steps {
//                 sh 'curl -u chethan:Chethan@22 -T target/**.war "http://172.173.179.196:8080/manager/text/deploy?path=/maheshbabuu&update=true"'
//             }
//         } 
//           stage('Stage-9 : SmokeTest') { 
//             steps {
//                 sh 'curl --retry-delay 10 --retry 5 "http://172.173.179.196:8080/maheshbabuu"'
//             }
//         }
//     }
// }
