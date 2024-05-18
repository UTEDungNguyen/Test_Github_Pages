// Script Pipeline
// node {
//     stage('Build') {
//         echo "hello"
//         deleteDir()
//         sh "git clone https://github.com/UTEDungNguyen/Test_Github_Pages.git"
//     }
//     stage('Test') {
//         echo "heiei"
//     }
//     stage('Deploy') {
//         echo "hehehe"
//     }
//     stage('test') {
//         // sh "#!/bin/bash"
//         // sh "cd Test_Github_Pages"
//         sh 'pwd'
//         steps {
//             dir('Test_Github_Pages') {
//                 sh "python3 test_py.py"
//             }
//         }
//     }
// }

// Deactivate Pipeline
pipeline {
    agent any

    stage('Build') {
        echo "hello"
        deleteDir()
        sh "git clone https://github.com/UTEDungNguyen/Test_Github_Pages.git"
    }
    stage('Test') {
        echo "heiei"
    }
    stage('Deploy') {
        echo "hehehe"
    }
    stage('test') {
        // sh "#!/bin/bash"
        // sh "cd Test_Github_Pages"
        sh 'pwd'
        steps {
            dir('Test_Github_Pages') {
                sh "python3 test_py.py"
            }
        }
    }
}

// post {
//     success {
//         echo 'Build succeeded!'
//     }
//     failure {
//         echo 'Build failed!'
//     }
// }