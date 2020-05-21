pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        git(credentialsId: 'zi2zi@lgcns.com', url: 'https://github.com/zi2zi/coremvc.git', branch: 'master')
      }
    }

    stage('Retore packages') {
      steps {
        sh 'dotnet restore dotnet_jenkins.csproj'
      }
    }

    stage('Clean') {
      steps {
        bat(script: 'dotnet clean dotnet_jenkins.csproj', encoding: 'UTF-8')
      }
    }

    stage('Publish') {
      steps {
        bat(script: 'dotnet clean dotnet_jenkins.csproj', encoding: 'UTF-8')
      }
    }

  }
  environment {
    dotnet = 'C:\\\\Program Files (x86)\\\\dotnet\\\\'
  }
}