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
        // sh "cd Test_Github_Pages"
        sh "cd Test_Github_Pages/python3 test_py.py"
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