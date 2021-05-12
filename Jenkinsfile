
pipeline {
    agent any

    stages {
        stage('frontend') {
            steps {
                echo 'executing yarn'
                nodejs('nodejs-10.17')
              {
                sh 'yarn install'
              }
            
            }
        }
          
          
        stage('backend') {
            steps {
                echo 'executing gradle'
              withgradle() {
                sh './gradle -v'
            }
        }
        }
 
    }
}
