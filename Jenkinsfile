pipeline {
    agent any
    stages {

        stage('Build') {
            steps {
                sh '''
                cd "Password Protection"
                mkdir -p build
                javac -d build src/*.java
                '''
            }
        }

        stage('Test') {
            steps {
                sh '''
                echo "Running Tests..."
                '''
            }
        }

        stage('Deploy') {
            steps {
                sh '''
                cd "Password Protection"
                jar cf FileEncrypter.jar -C build .
                '''
            }
        }
    }
}
