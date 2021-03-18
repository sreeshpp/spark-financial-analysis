#!/usr/bin/env groovy

node{
    stage('Prepare'){
        cleanWs()
        git(
        url: 'https://github.com/sreeshpp/spark-financial-analysis.git',
        credentialsId: 'sreeshpp',
        branch: 'master'
        )
    }
    stage('Build'){
        if(isUnix()){
        echo 'unix os'
        sh 'pwd'
        sh './gradlew clean build -xtest --info'
  }
  else{
    echo 'not a unix os'
  }
    }
}
