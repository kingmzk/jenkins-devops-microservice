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

// 


pipeline {
    agent {
        docker {
            image 'maven:3.6.3'
            args '-v /var/run/docker.sock:/var/run/docker.sock'
        }
    }
    options {
        // Set the working directory to an absolute path
        // Replace this path with your actual project directory
        dockerfile {
            dir 'E:\\DEVOPS\\jenkins'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }
    }
}
