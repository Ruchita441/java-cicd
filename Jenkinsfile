pipeline{
   
   agent any
   stages{
   
      stage('Git Checkout'){
        
        steps{
            git branch: 'main', url: 'https://github.com/Ruchita441/java-cicd.git'
        }
      }  
      stage('Unit Testing'){
        
        steps{
            sh 'mvn test'
        }
      }  
      stage('Integration Testing'){
        
        steps{
            sh 'mvn verify -DskipUnitTests'
        }
      }  
      stage('Maven Build'){
        
        steps{
            sh 'mvn clean install'
        }
      }  
      stage('SonarQube Anyalsis'){
        
        steps{
           scripts{
            withSonarQubeEnv(credentialsId: 'sq') {
              sh 'mvn clean package sonar:sonar'
}
        }
        }
      }  
   }
}
