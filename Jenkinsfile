pipeline{
  agent{'label = Jenkins-Agent}
  tools{
    jdk 'java17'
    maven 'maven3'
  }
  stage{
    stage('Cleanup Workspace'){
      step{
        cleanWs()
      }
  }
  stage{
    stage('Checkout from SCM'){
      step{
        git branch: 'main', cendentialId: 'github', url: 'https://github.com/esu8500/register-app'
      }
  }
  stage{
    stage('Build Application'){
      step{
        sh "maven clean package"
      }
    }
    stage{
    stage('Test Appcation'){
      step{
        sh "mvn Test"
      }
    }
  }  
    
