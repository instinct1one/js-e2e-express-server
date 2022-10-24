pipeline {
    agent { label 'NPM' }
    stages {
        stage('Clone Repo') {
            steps {
                git url: "https://github.com/GitPracticeRepo/js-e2e-express-server.git", 
                branch: "main"
            }
        }
        stage('Install') {
            steps {
                sh "export PATH='/home/ubuntu/.nvm/versions/node/v16.0.0/bin:$PATH' npm install"
            }
        }
        stage('Build') {
            steps {
            sh "export PATH='/home/ubuntu/.nvm/versions/node/v16.0.0/bin:$PATH' npm run build"
            }
        }
        stage('Test') {
            steps {
            sh "export PATH='/home/ubuntu/.nvm/versions/node/v16.0.0/bin:$PATH' npm test"
        }
    }
}
}