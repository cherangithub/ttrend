def registry = 'https://valaxy01.jfrog.io'
def imageName = 'valaxy01.jfrog.io/valaxy-docker-local/ttrend'
def version   = '2.1.2'
pipeline {
    agent {
        node {
            label 'maven-agent'
        }
    }

environment {
    PATH = "/opt/apache-maven-3.9.1/bin:$PATH"
}
    stages {
        stage('build'){
            steps {
                echo '------------------- Build Started -------------'
                sh 'mvn clean deploy -Dmaven.test.skip=true'
                echo '------------------- Build Completed -------------'
            }
        }
    }
}
