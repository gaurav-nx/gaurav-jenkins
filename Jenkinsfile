pipeline {
    agent any
    environment {
        PATH = "/opt/maven/bin:$PATH"
    }
    stages {
        stage('Git clone') {
            steps {
                git url: 'https://github.com/koddas/war-web-project.git', branch: 'master'
            }
        }
        
        stage('build') {
            steps {
                sh 'mvn clean install'
            }
        }
    }
}
