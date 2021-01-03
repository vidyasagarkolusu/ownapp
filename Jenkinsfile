node{
  stage('SCM Checkout'){
    git 'https://github.com/vidyasagarkolusu/ownapp.git'
  }
  stage('Compile-Package'){
    sh 'mvn package'
  }
}
