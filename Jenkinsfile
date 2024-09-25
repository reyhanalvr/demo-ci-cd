def secret = 'test'
def vmapps = 'ubuntu@3.1.90.43'
def dir    = '/home/ubuntu/dumbflix-frontend'
def branch = 'master'
#def images = 'dumbflix-fe'
#def tag    = 'latest'

pipeline {
    agent any
    stages {
        stage ("pull") {
           steps {
               sshagent([secret]){
                  sh """ssh -o StrictHostKeyChecking=no ${vmapps} << EOF
                  echo test
                  exit
                  EOF"""
                }
            }
        }
    }
}
