node{
  stage('SCM Checkout'){
    git 'https://github.com/vidyasagarkolusu/ownapp.git'
  }
  stage('Compile-Package'){
    sh 'mvn package'
  }
  sshagent(['ec2-user']) {
   sh 'scp -o StrictHostKeyChecking=no  target/*.war ec2-user@3.94.181.81:/opt/tomcat8/webapps/'
}
  stage('Email Notification'){
     mail bcc: '', body: '''Hi Welcome to Jenkins alerts 
Thanks
Vidyasagar''', cc: '', from: '', replyTo: '', subject: 'Jenkins Job', to: 'vidyasagar.kolusu@gmail.com'
  }
}
