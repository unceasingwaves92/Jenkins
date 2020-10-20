pipeline {
  agent any
  stages {
    stage('Development') {
      steps {
        echo 'This is development'
      }
    }

    stage('QA') {
      parallel {
        stage('UI Automation') {
          steps {
            echo 'This is UI Automation'
          }
        }

        stage('API Automatiion') {
          steps {
            echo 'REST API Automation'
          }
        }

        stage('Performance Testing') {
          steps {
            echo 'JMeter Load testing'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploy to Prod'
      }
    }

  }
}