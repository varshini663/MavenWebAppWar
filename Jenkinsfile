pipeline {
    agent any

    tools {
        maven 'Maven'
        jdk 'JDK'
    }

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/varshini663/MavenWebAppWar.git'
            }
        }

        stage('Build WAR') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Deploy WAR') {
            steps {
                sh 'cp target/my-webapp-1.0-SNAPSHOT.war /opt/tomcat/webapps/'
            }
        }

        }
    }
