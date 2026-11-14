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
            echo 'Building Python application'
            bat '"C:\\Users\\student\\AppData\\Local\\Programs\\Python\\Python313\\python.exe" -m py_compile app.py'
        }
    }

    stage('Test') {
        steps {
            echo 'Testing Python application'
            bat '"C:\\Users\\student\\AppData\\Local\\Programs\\Python\\Python313\\python.exe" app.py'
        }
    }

    stage('Deploy') {
        steps {
            echo 'Deploying Python application'
            echo 'Python application deployed successfully'
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
