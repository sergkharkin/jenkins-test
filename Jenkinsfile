pipeline {
  agent {label 'inteliventi'}
  stages {
        stage("Checkout Git") {
            steps {
                git branch: 'bh-devops-02-22', url: 'https://github.com/sergkharkin/belhard-devops.git' 
            }
        }
        stage("List repository") {
            steps {
                sh '''
                ls -la
                docker ps -a
                '''
            }
        }
    }
    post { 
        always { 
            cleanWs()
        }
    }
}
