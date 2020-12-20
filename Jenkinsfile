pipeline
{
    agent any

    tools {
        gradle 'Gradle 6.2'
    }

    stages
    {
        stage ('run frontend')
        {
           steps
           {
                echo 'executing yarn....'
                nodejs('Node-10.17'){
                    sh 'yarn install'
                }
               echo 'testing executing yarn....'

           }
        }
        stage ('run backend')
        {
            steps
            {
                echo 'executing gradle...'
                withGradle()
                {
                    sh './gradlew -v'
                }
            }
        }
    }
}

