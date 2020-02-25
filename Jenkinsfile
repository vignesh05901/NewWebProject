node{
  def mvn_Home= tool name: 'Maven', type: 'maven'
  stage('Git checkout'){
    git "https://github.com/vignesh05901/NewWebProject"
  }
  
  stage('Build'){
    sh "${mvn_Home}/bin/mvn clean"
    sh "${mvn_Home}/bin/mvn validate"
    
  }
  
  stage('Test'){
    sh "${mvn_Home}/bin/mvn verify"
  }
  
  stage('Package'){
    sh "${mvn_Home}/bin/mvn package"
  }
}
