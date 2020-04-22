pipeline {
  agent any
  stages {
    stage('Upload to AWS') {
      steps {
        withAWS(region:'us-west-2') {
            s3Upload(file:'index.html', bucket:'pipelineproject',path:'index.html')
             }
      steps {
        sh 'echo "Hello World"'
        sh '''
                    echo "Multiline shell steps works too"
                    ls -1ah
                '''
       
    }

  }
}