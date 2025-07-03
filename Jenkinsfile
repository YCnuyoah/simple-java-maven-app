pipeline {
    agent any  

    stages {
        stage('Build') {
            steps {
                
                sh '''
                    docker run --rm \
                    -v /root/.m2:/root/.m2 \
                    -v $PWD:/app \
                    -w /app \
                    maven:3-alpine \
                    mvn -B -DskipTests clean package
                '''
            }
        }
    }
}
