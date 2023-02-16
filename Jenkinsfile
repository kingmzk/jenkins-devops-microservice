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
    // agent { docker { image  'maven:3.6.3'} }
    // agent { docker { image  'node:13.8'} }
    environment {
        dockerHome = tool 'myDocker'
        mavenHome =  tool 'myMaven'
        PATH = "$dockerHome/bin:$mavenHome/bin:$PATHco"
    }



    stages{
        stage('Build') {
            steps {
                // sh 'mvn --version'
                // sh 'pwd'
                // bat 'cd'
                // bat 'mvn --version'
                // bat 'node --version'
                bat 'docker version'
                echo "Build"
                echo "PATH - $PATH"
                echo "BUILD_NUMBER - $env.BUILD_NUMBER"
                echo "BUILD_ID - $env.BUILD_ID"
                echo "JOB_NAME - $env.JOB_NAME"
                echo "BUILD_TAG - $env.BUILD_TAG"
                echo "BUILD_URL - $env.BUILD_URL"
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