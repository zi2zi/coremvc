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
        sh 'dotnet clean dotnet_jenkins.csproj'
      }
    }

    stage('Publish') {
      steps {
        sh 'dotnet publish dotnet_jenkins.csproj'
      }
    }

  }
  environment {
    dotnet = 'C:\\\\Program Files (x86)\\\\dotnet\\\\'
  }
}