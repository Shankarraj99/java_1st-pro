pipeline {
    agent any

    stages {
        stage('gitjob') {
            steps {
                echo 'Cloning...'
                git 'https://github.com/Shankarraj99/java_1st-pro.git'
            }
        }
        stage('buildjob') {
            steps {
                echo 'Building...'
                sh 'mvn compile'
            }
        }
        stage('testjob') {
            steps {
                echo 'testing...'
                sh 'mvn test'
            }
        }
        stage('deployjob') {
            steps {
                echo 'deploying...'
                sh 'mvn package'
                archiveArtifacts artifacts: 'target/addressbook.war', followSymlinks: false
            }
        }
    }
}
