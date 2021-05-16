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
                withGradle() {
                   sh './gradlew -v'
            }
        }
        }
 
    }
}
