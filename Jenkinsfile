pipeline {
    agent any
    tools{
        jdk 'JDK_17'
        maven 'apache-maven-3.8.5'
    }
    stages {
        stage('Initialization') {
            steps {
                echo "\033[44mJAVA_HOME = ${M2_HOME}\033[0m"
                echo "M2_HOME = ${M2_HOME}"
            }
        }
        stage('Build') {
            steps {
                sh 'mvn -DskipTests clean compile'
            }
        }
        stage('Package') {
            steps {
                sh 'mvn package'
            }
        }
    }
}
