 pipeline{
   stage('SCM Checkout'){
     git 'https://github.com/amenaafreen/my-app'
   }
   stage('Compile-Package'){
    
    /get maven path 
    
    def mvnHome = tool name: 'maven-3', type: 'maven'
    sh "${mvnHome}/bin/mvn package"
   
  }
}


