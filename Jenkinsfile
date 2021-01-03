node{
  stage('SCM Checkout'){
    git 'https://github.com/vidyasagarkolusu/ownapp.git'
  }
  stage('Compile-Package'){
    sh 'mvn package'
  }
  stage('Email Notification'){
     mail bcc: '', body: '''Hi Welcome to Jenkins alerts 
Thanks
Vidyasagar''', cc: '', from: '', replyTo: '', subject: '', to: 'vidyasagar.kolusu@gmail.com'
  }
}
