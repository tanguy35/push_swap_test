pipeline {
  agent {
    docker {
        image 'silkeh/clang:16'
        label "linux"
        reuseNode true
    }
  } 
    stages {
      stage('Dependencies') {
        steps {
            sh "apt-get install -y make"
        }
      }
      stage('Compile') {
        steps {
            sh make
        }
      } 
    }
}
