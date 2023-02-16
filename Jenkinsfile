//SCRIPTED  old aproarch

// node{
//     echo('Build')
//     echo('Test')
//     echo('Integration Test')
// }

// node {
//     stage('Build') {
//         echo "Build"
//     }

//     stage('Test') {
//        echo "Test"
//     }

//     stage('Integration Test') {
//         echo "Integration Test"
//     }
// }

//DECLARATIVE

pipeline {
    // agent any
    // agent { docker { image  'maven:3.6.3'} }
    agent { docker { image  'node:13.8'} }
    stages{
        stage('Build') {
            steps {
                // sh 'mvn --version'
                // sh 'pwd'
                bat 'cd'
                // bat 'mvn --version'
                bat 'node --version'
                echo "Build"
            }
        }

        stage('Test'){
            steps {
                echo "Test"
            }
        }

        stage('Integration TEst'){
            steps {
                echo "Integration Test"
            }
        }
    }  
    
    post {
        always {
            echo 'I am Good . I always Run No Matter What'
        }
        success {
            echo "I RUn only when you are successfull"
        }
        failure {
            echo "I Only Run When You Fails the BUild"
        }

        changed {                             // means when status changed 
            echo  "status is changed either fail to success or success to fail"
        }              
    }

}