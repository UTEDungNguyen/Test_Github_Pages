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
        sh "cd /var/lib/jenkins/workspace/test_pipeline/Test_Github_Pages"
        sh 'pwd'
        dir
        sh "python3 test_py.py"
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