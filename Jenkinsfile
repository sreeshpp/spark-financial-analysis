#!/usr/bin/env groovy

node{
    stage('Prepare'){
        cleanWs()
        git(
        url: 'git@github.com:sreeshpp/spark-financial-analysis.git',
        credentialsId: '40fcc00956465460ebc72f6bf220c6b4c6bbe7d7',
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
