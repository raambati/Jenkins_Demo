pipeline {
    agent any
    stages {
        stage('run frontend') {
            steps {
                echo 'Executing yarn.....'
            }
        }
        stage('run backend') {
            steps {
                echo 'Executing gradle.....'
                    withGradle(){
                        sh './gradlew -v'
                    }
                }
            }
        }
    }
}
