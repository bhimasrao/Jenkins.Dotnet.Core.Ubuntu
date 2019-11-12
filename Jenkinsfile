pipeline {
    agent { node { label 'slave_new' } }
    
        parameters { choice(choices: 'dev\nqa', description: 'What environment?', name: 'DEPLOY_TO') } 
        
        stages { 

    stage('Checkout') { 

      steps { 

        checkout([ 

          $class: 'GitSCM', 

          branches: [[name: '*/master']], 

          userRemoteConfigs: [[credentialsId: '901eea44-a582-448f-997d-7016c48363e5', 

          url: 'https://github.com/busani9/Jenkins.Dotnet.Core.Ubuntu.git']] 

        ]) 

      } 

    } 
    
    }
    
    }
    
