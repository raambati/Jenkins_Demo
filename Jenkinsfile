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
                nodejs('Node-10.17'){
                    sh 'yarn install'
                }
               echo 'testing executing yarn....'

           }
        }
        stage ('run backend')
        {
            steps {
                echo 'executing gradle...'
                withGradle(){
                    sh './gradle -v'
                }
        }
    }
}

