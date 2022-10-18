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
   }
}
