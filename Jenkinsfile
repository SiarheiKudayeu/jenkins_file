pipeline {
    agent { 
        node {
            label 'docker-agent-alpine'
            }
      }
    triggers {
        pollSCM '* * * * *'
    }
    stages {
        stage('Build') {
            steps {
                echo "Building.."
                sh '''
                '''
            }
        }
                stage('Cloning repo') {
            steps {
                echo "Clone.."
                sh '''
                git clone https://github.com/SiarheiKudayeu/jenkins.git
                '''
            }
        }
                stage('Go To the test directory and start test') {
            steps {
                 echo "Go To the test director"
                sh '''
                cd jenkins/src
                javac Test.java
                java Test
                ls
                '''
            }
        }
        stage('Deliver') {
            steps {
                echo 'Deliver....'
                sh '''
                echo "doing delivery stuff.."
                '''
            }
        }
    }
}