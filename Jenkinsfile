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
        cd Test_Github_Pages
        // sh "ls"
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