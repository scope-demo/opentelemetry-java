pipeline {
    agent none
    stages {
        stage('Opentelemetry Scope Tests') {
            agent { docker 'openjdk:8-jdk' }
            steps {
                sh '''
                    git submodule init
                    git submodule update
                    ./gradlew clean assemble check --stacktrace
                '''

                //sh 'make init-git-submodules'
                //sh 'make test verify-format'
            }
        }
    }
}
