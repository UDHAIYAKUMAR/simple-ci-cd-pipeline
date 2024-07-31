
pipeline {
    agent any
    environment {
        PATH = "/usr/local/bin:$PATH"
    }
    stages {
        stage('Build') {
            steps {
                sh '/usr/local/bin/npm install'
            }
        }
        stage('Test') {
            steps {
                sh '/usr/local/bin/npm test'
            }
        }
        stage('Docker Build') {
            steps {
                sh 'docker build -t myapp .'
            }
        }
        stage('Deploy') {
            steps {
                sh 'docker run -d -p 80:3000 myapp'
            }
        }
    }
}


pipeline {
    agent any
    environment {
        PATH = "/usr/local/bin:${env.PATH}"
    }
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                sh 'npm test'
            }
        }
        stage('Docker Build') {
            steps {
                sh 'docker build -t myapp .'
            }
        }
        stage('Deploy') {
            steps {
                sh 'docker run -d -p 80:3000 myapp'
            }
        }
    }
}

pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                sh 'npm test'
            }
        }
        stage('Docker Build') {
            steps {
                sh 'docker build -t myapp .'
            }
        }
        stage('Deploy') {
            steps {
                sh 'docker run -d -p 80:3000 myapp'
            }
        }
    }
}

