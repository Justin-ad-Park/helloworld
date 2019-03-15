#!groovy

node {
  stage 'Checkout'
    checkout scm

  stage 'Setup'
    sh 'export PATH=/usr/local/bin:$PATH'
    sh 'echo $PATH'

  stage 'Mocha test'
    sh './node_modules/mocha/bin/mocha'
  
  stage 'Cleanup'
    echo 'prune and cleanup'
    sh 'rm node_modules -rf'
}
