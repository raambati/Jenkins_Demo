pipeline
{
    agent any

    stages
    {
        stage('Rajesh First Job')
        {
            steps
            {

                git clone https://github.com/raambati/Jenkins_Demo.git
            }
        }

        stage('Rajesh Second Job')
        {
            steps
            {

                mvn clean install
            }
        }
    }
}