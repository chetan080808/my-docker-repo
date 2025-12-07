pipeline {
  agent any
  stages{
    stage("Build") {
      steps {
        sh ''' 
          ls -ltr
          docker build -t hello .
          docker images
        '''
      }
    }
    stage("Deploy") {
      steps {
        sh ''' 
          docker run -d --name cont2 hello
        '''
      }
    }
    stage("Cleanup") {
      steps {
        sh ''' 
          docker rm -f cont2
        '''
      }
    }
  }
}
