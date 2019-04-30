node{
   stage('SCM Checkout'){
     git 'https://github.com/amenaafreen/jenkins-pipeline-maven'
   }
   stage('Compile-Package'){
    
      def mvnHome =  tool name: 'maven-3', type: 'maven'   
      sh "${mvnHome}/bin/mvn package"
   } 
   
   sshagent(['tomcat']) {
    sh 'scp -o StrictHostKeyChecking=no -l target/*.war ec2-user@http://3.14.79.156:/usr/share/tomcat/webapps'
}
}




