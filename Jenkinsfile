pipeline {
    agent { node { label 'slave_new' } }
    
        
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
      
            stage('build') {
                steps { 
sudo systemctl stop test.service
sudo systemctl stop nginx
sudo dotnet publish --configuration release
sudo systemctl start test.service
sudo systemctl start nginx
                }
            }
            
    
    }
    
    }
    
