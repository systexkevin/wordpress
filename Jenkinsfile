pipeline {
  agent {
    kubernetes {
      	cloud 'openshift'
      	defaultContainer 'jnlp'
      }
    }
  stages {
    stage('Deploy App') {
      steps {
        script {
          kubernetesDeploy(configs: "mysql-deployment.yml", kubeconfigId: "MINIKUBECONFIG")
        }
      }
    }
  }
}
