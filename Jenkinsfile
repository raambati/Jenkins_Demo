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
                script{
                    def browsers = {'chrome','firefox'}
                    for (int i = 0; i < browsers.size(); ++i ){
                        echo = "Testing the $browsers[i] browser"
                    }
                }
            }
        }

        stage('Rajesh Second Job')
        {
            steps
            {
                echo 'Building the Application'
            }
        }
    }
}