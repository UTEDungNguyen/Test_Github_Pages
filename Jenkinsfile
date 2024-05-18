// Script Pipeline
node {
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
        // sh 'pwd'
        dir('Test_Github_Pages') {
            dir('yaml') {
                stage('test_1'){
                    sh "sudo chmod o+rx test1.yaml"
                    script {
                        def yamlContent = readFile('test1.yaml').trim()
                        def yaml = readYaml text: yamlContent
                        yaml.steps.each { step ->
                            sh step.sh
                        }
                    }
                    // sh "python3 test_py.py"
                }

                // stage('test_2'){
                //     sh "sudo chmod o+rx test2.yaml"
                //     sh "python3 test_py.py"
                // }
                
            }
            // sh "python3 test_py.py"
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