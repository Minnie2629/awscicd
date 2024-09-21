pipeline {
 agent any 

 environment {
    BRANCH_NAME = 'main'
    GIT_URL = 'https://github.com/Minnie2629/awscicd.git'
    IMAGE_TAG = 'awscicd'  
    IMAGE_vERSION = "${BUILD_NUMBER}"
 }

  stages {
   stage('git checkout'){
    steps{
        git branch: "${BRANCH_NAME}", url: "${GIT_URL}"
    }
   }
   stage('docker build'){
    steps{
        sh 'docker build -t "${IMAGE_TAG}:${BUILD_NUMBER}" .'
        sh 'docker images'

    }
   }
  }
}
