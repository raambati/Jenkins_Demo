pipeline
{
    agent any

    stages
    {
        stage('Rajesh First Job')
        {
            steps
            {
                echo 'Git Checkout'
                git clone https://github.com/raambati/Jenkins_Demo.git
            }
        }

        stage('Rajesh Second Job')
        {
            steps
            {
                echo 'Building the Application'
                mvn clean install
            }
        }
    }
}