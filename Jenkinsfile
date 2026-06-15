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
            echo 'Building project...'
        }
    }

    stage('Test') {
        steps {
            echo 'Running tests...'
        }
    }

    stage('Deploy') {
        steps {
            echo 'Deploying application...'
        }
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
