node{
     def mavenHome = tool name :"maven3.8.5"
     stage('CheckoutCode')
     {
      git branch: 'development', credentialsId: 'a46b5ca3-e808-4341-9629-a6dbed4869c9', url: 'https://github.com/devops-ecomerce-apps/maven-web-application.git'
      }
      stage('Build'){
      sh "${mavenHome}/bin/mvn clean package" 
      }
     stage('Emailnotification'){
emailext body: 'build completed', subject: 'build is oveer', to: 'msoma6464@gmail.com'
}

     /* stage('ExecuteSonarQubeReport'){
      sh "${mavenHome}/bin/mvn clean package sonar:sonar" 
      }
      stage('UploadArtifactIntoNexus'){
      sh "${mavenHome}/bin/mvn clean deploy" 
      }
      stage('DeployAppintoTomcat'){
   sshagent(['6b07c9e1-ea53-4777-a5d4-7f5268a954d4']) {
   sh "scp -o StrictHostKeyChecking=no target/maven-web-application.war ec2-user@13.127.123.163:/opt/apache-tomcat-9.0.62/webapps/"
}
}
stage('Emailnotification'){
emailext body: 'build completed', subject: 'build is oveer', to: 'msoma6464@gmail.com'
}
*/
}
