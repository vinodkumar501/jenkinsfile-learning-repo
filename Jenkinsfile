//https://www.youtube.com/watch?v=L9Ite-1pEU8
pipeline {
   agent any 
   tools {
       gradle('gradle-7.3')  
   }
   stages{
      stage("run frontend"){
       steps{
         echo 'executing yarn ..'
         nodejs('node-17.1.0'){
             sh 'yarn install'
             sh 'npm config ls'
             sh 'npm -version'
         }
       }
    }
      stage("run backend"){
       steps{
         echo 'executing graddle'
         //sh 'gradle wrapper'
         //sh 'chmod +x ./gradlew'
         //sh './gradlew -v'  
         sh 'gradle clean build'
         //https://docs.gradle.org/current/userguide/jenkins.html
         }
      }
    }
  }  
