pipeline {
    agent any
        parameters {
               choice(name: 'VERSION', choices: ['1.1.0','2.1.0','2.4.5'], description: 'version to be deployed on prod')
               booleanParam(name: 'executeTests', defaultvalue:true, description: '')
                }

    stages {
        stage('Build') {
             when   {
              expression {
                          params.executeTests = true                                                                         
                           }  
            steps {
                echo 'Building45 and..'
            }
        }
        }
        stage('Test') {
            steps {
                echo 'Testing45 and ..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying45 and....'
                echo 'deploying version ${params.VERSION}'
            }
        }
    }
}
