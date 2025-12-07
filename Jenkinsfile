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
  }
}
