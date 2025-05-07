pipeline {
  agent any 

  environment {
    OPENSHIFT_SERVER = "https://api.ocp4.example.com:6443"
    OPENSHIFT_NAMESPACE = "development"
    OPENSHIFT_TOKEN = credentials("jenkins-ocp-token")
  }

  stages {
    stage('Login into OCP') {
      steps {
        script {
          sh "oc login --token=${OPENSHIFT_TOKEN} --server=${OPENSHIFT_SERVER}"
        }
      }
    }
  }
}
