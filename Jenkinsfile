pipeline
{
    agent any

    stages
    {
        stage('checkout source code')
        {
            steps
            {
                git clone https://github.com/raambati/Jenkins_Demo.git
            }
        }

        stage('build the source code')
        {
            steps
            {
                mvn clean install
            }
        }
    }
}