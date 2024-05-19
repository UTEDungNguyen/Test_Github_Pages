// Script Pipeline
node {
    try
    {
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
            dir('Test_Github_Pages') {
                stage('test1'){
                    sh "python3 test_py.py"
                }

                stage('test2'){
                    sh "python3 babaa.py"
                }
                
            }
        }
    }

    catch (Exception e) 
    {
        // Handle Error while running process
        echo "Build failed due to: ${e.message}"
        currentBuild.result = 'FAILURE'
    }

    finally
    {   
        // Run success
        if(currentBuild.result == 'SUCCESS')
        {
            echo "Running Jobs SUCCESS"
        }

        // Run Failed
        if(currentBuild.result == 'FAILURE')
        {
            echo "Running Jobs Failed"
        }

        // Connect Unstable
        if(currentBuild.result == 'UNSTABLE')
        {
            echo "Connect Unstable"
        }

        // Finish Jobs
        else 
        {
            echo "One way or another, Finished Running Jobs"
        }
    }
}

// Deactivate Pipeline
// pipeline {
//     agent any

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

// post {
//     success {
//         echo 'Build succeeded!'
//     }
//     failure {
//         echo 'Build failed!'
//     }
// }