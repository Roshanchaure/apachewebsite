Pipeline {
  agent any
  stages{
    stage('Clone repository'){
      steps{
        git 'https://github.com/Roshanchaure/apachewebsite.git'
      }
    }
    stage('Install Apache'){
      steps{
        sh '''
        sudo apt update
        sudo apt install apache2 -y
        '''
      }
    }
    stage('Deploy application'){
    steps{
      sh '''
      sudo rm -rf /var/www/html/*
      sudo cp -r * /var/www/html/
      sudo systemctl restart apache2
      '''
    }
  }
}
}



