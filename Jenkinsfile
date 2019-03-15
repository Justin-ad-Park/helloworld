#!groovy

node {
  stage 'Checkout'
    checkout scm

  stage 'Setup'
    sh 'export PATH=/home/ec2-user/.nvm/versions/node/v11.12.0/bin:/usr/local/bin:/bin:/usr/bin:/usr/local/sbin:/usr/sbin:/sbin:/home/ec2-user/.local/bin:/home/ec2-user/bin:$PATH'
    sh 'echo $PATH'
    sh 'npm install'

  stage 'Mocha test'
    sh './node_modules/mocha/bin/mocha'
  
  stage 'Cleanup'
    echo 'prune and cleanup'
    sh 'npm prune'
    sh 'rm node_modules -rf'
}


