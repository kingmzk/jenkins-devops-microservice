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
    agent any
    stages{
        stage('Build') {
            steps {
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
    }  post {
        always {
            echo 'I am Good . I always Run No Matter What'
        }
        success {
            echo "I RUn only when you are successfull"
        }
        failure {
            echo "I Only Run When You Fails the BUild"
        }
    }

}