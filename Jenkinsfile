pipeline {
  agent {
    docker {
        image 'silkeh/clang:latest'
        label 'linux'
    }
}
    
    stage('Compile') {
            steps {
                sh "apt-get install -y make"
                sh 'make'
            }
        }


}
