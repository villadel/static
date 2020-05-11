pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
               sh  'echo "========Hello WOrld========'
               sh '''
                    echo "Multiline shell steps works too"
                    ls -lah
                   '''

            }
            
        }
    }
    post{
      
        success{
            echo "========pipeline executed successfully ========"
        }
        failure{
            echo "========pipeline execution failed========"
        }
    }
}