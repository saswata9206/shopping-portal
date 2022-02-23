pipeline{

    agent any

// uncomment the following lines by removing /* and */ to enable
   tools{
       nodejs 'nodejs' 
    }
   

    stages{
        stage('compile-app'){
            steps{
                echo 'this is the comile job'
                sh 'npm install'
            }
        }
        stage('test-app'){
            steps{
                echo 'this is the testjob'
                sh 'npm test'
            }
        }
        stage('package-app'){
            steps{
                echo 'this is the package job'
                sh 'npm run package'
            }
        }
    }
    
    post{
        always{
            echo 'I know how to create pipeline'
        }
        
    }
    
}
