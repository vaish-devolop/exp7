pipeline { agent any
          stages {

    stage('Checkout') {
        steps {
            echo 'Downloading source code from GitHub'
            checkout scm
        }
    }

    stage('Build') {
        steps {
            echo 'Compiling Java application'
            bat 'javac App.java'
        }
    }

    stage('Test') {
        steps {
            echo 'Running Java application'
            bat 'java App'
        }
    }

    stage('Deploy') {
        steps {
            echo 'Deploying Java application'
            echo 'Deployment completed successfully'
        }
    }
}

post {
    success {
        echo 'BUILD SUCCESSFUL!'
    }

    failure {
        echo 'BUILD FAILED!'
    }

    always {
        echo 'Jenkins pipeline execution completed'
    }
}
}
