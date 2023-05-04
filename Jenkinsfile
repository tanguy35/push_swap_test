pipeline {
          agent {
            docker {
                image 'silkeh/clang'
                label 'linux'
            }
        }
        
        stages {
          stage('Compile')
          {
            steps {
                sh "apt-get install make"
                sh make
           }
        }               
}
