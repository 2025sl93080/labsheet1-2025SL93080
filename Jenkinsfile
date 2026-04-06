pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Cloning repository...'
                git branch: 'main', url: 'https://github.com/2025sl93080/labsheet1-2025SL93080.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Building project...'
                sh 'ls'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                sh '''
                python3 - <<EOF
import calculator

assert calculator.add(2,3) == 5
assert calculator.multiply(2,3) == 6
assert calculator.subtract(5,3) == 2
assert calculator.divide(6,2) == 3

print("All tests passed!")
EOF
                '''
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploy stage (dummy for now)...'
            }
        }
    }
}
