pipeline {
    agent any
    stages {
        stage('One') {
            steps{
                echo 'YOOO!!!! Bled'
                //bat 'mvn clean package'
            }
        }
        stage('Two') {
            steps{
                echo 'YOOO!!!! Zaniar!!'
                //bat 'mvn clean package'
            }
        }
    }

  post {
    success {
      slackSend color: "#00FF00", channel: "#test-jenkins", message: "Build Success: Job ${env.JOB_NAME} [${env.BUILD_NUMBER}] (${env.BUILD_URL})"
    }

    failure {
      slackSend color: "#FF0000", channel: "#test-jenkins", message: "Build failure: Job ${env.JOB_NAME} [${env.BUILD_NUMBER}] (${env.BUILD_URL})"
    }
  } 
}
