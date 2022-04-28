pipeline {
    agent any
    stages {
        stage('Example') {
            steps {
                echo "Running ${env.BUILD_ID} on ${env.JENKINS_URL}"
            }
        }
        stage('Build') {
                    steps {
                        sh 'mvn -DskipTests clean package'
                    }
                }
    }
}