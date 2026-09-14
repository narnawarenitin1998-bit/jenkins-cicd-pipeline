pipeline {
agent any

stages {

    stage('Checkout') {
        steps {
            git branch: 'main',
                url: 'https://github.com/narnawarenitin1998-bit/jenkins-cicd-pipeline.git'
        }
    }

   stage('Build') {
    steps {
        bat 'docker build -t jenkins-demo .'
    }
}
    stage('Test') {
        steps {
            echo 'Running tests...'
        }
    }

  stage('Deploy') {
    steps {
        bat 'docker rm -f jenkins-demo-container || exit /b 0'
        bat 'docker run -d --name jenkins-demo-container -p 8085:80 jenkins-demo'
    }
}

post {
    success {
        echo 'Pipeline executed successfully!'
    }

    failure {
        echo 'Pipeline execution failed!'
    }

    always {
        echo 'Pipeline execution completed.'
    }
}


}
