#!groovy

node {
  stage 'Checkout'
    checkout scm

  stage 'Setup'
    sh 'export PATH=/usr/local/bin:$PATH'
    sh 'npm install'

  stage 'Mocha test'
    sh './node_modules/mocha/bin/mocha'
  
  stage 'Cleanup'
    echo 'prune and cleanup'
    sh 'npm prune'
    sh 'rm node_modules -rf'
}
