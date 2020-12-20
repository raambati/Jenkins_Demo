pipeline
{
    agent any
    stages
    {
        stage ('run frontend')
        {
           steps
           {
                echo 'executing yarn....'
               echo 'testing executing yarn....'

           }
        }
        stage ('run backend')
        {
            steps {
                echo 'executing gradle...'
                echo 'This is repeated test to build and upload to Artefact'
            }
        }
    }
}

