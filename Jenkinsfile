pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
          sh 'g++ ./main/hello.cpp -o ./main/hello'
          echo 'Build successful'
          build job: 'error'
            }
          }
stage('Test') {
    steps {
		sh './main/hello'
		echo 'Test successful'
			}
}
stage ('Deploy') {
      steps {
        echo 'Deployment Successful'
      }
   }
}
post {
    failure {
echo 'Pipeline failed'
    }
  }
}
