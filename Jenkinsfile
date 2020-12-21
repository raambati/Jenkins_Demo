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
                nodejs('Node-10.17')
                {
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
                    sh '''
                       conda create --yes -n ${BUILD_TAG} python
                       source activate ${BUILD_TAG}
                       // example of unit test with nose2
                       pip install nose2
                       nose2
                    '''
                }
            }
        }
    }
}