pipeline {
  agent any
  stages {
      stage('Nettoyage')
      {
          steps {
              sh 'export TERM=xterm;make clean'
          }
      }
      stage('Compilation de push_swap_test')
      {
          steps {
              sh 'export TERM=xterm;make push_swap_test'
          }
      }
      stage('Compilation de checker')
      {
          steps {
              sh 'export TERM=xterm;make checker'
          }
      }
      stage('Test 1')
      {
          steps {
              sh './push_swap 45 3 8 2 5 6 9 1 | ./checker 45 3 8 2 5 6 9 1'
          }
      }
      stage('Test 2')
      {
          steps {
              sh './push_swap 45 3 8 2 5 6 9 1 | ./checker 54 3 0 2 5 6 9 1'
          }
      }
   }
}
