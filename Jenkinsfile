node {
      stage('Scm Checkout'){
      git credentialsId: '70879577-c865-415b-b4cb-0c6e86882477', url: 'https://www.github.com/Bharat-vyas/repo-2.git'
      }
      stage('view all docker containers'){
      sh label: '', script: 'docker ps -a'
      }
      stage('Create Docker Image and run container out of it in local system'){
      sh label: '', script: 'docker build -t bharatvyas/image1 .'
      sh label: '', script: 'docker run -itd bharatvyas/image1'      
      }
      stage('Push image to dockerhub'){
      withDockerRegistry(credentialsId: '996ea76f-df01-4824-9db3-0bc3a7c24c21') {
      sh 'docker push bharatvyas/image1'
      }
      }
}
