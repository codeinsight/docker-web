#!/usr/bin/groovy
@Library('github.com/fabric8io/fabric8-pipeline-library@v2.2.311')
def utils = new io.fabric8.Utils()
dockerNode{
  checkout scm
  container(name: 'docker') {
        sh 'docker ps'
        sh 'docker-compose up'
    }
}