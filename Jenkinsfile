//    1. Create a Jenkins Pipeline Job
//    2. Configure Jenkins declarative pipeline
//        a. Where my pipeline should be running
//        b. What are the tools that pipeline should be using
//        c. My pipeline will always maintain 10 Max builds
//        d. Checkout the Sourcecode from the git
//        e. Build the Sourcecode using maven

pipeline
{
    agent any
    tools
    {
        jdk 'JDK9'
        maven 'Maven3'
    }
    options
    {
        timestamps()
        buildDiscarder(logRotator(daysToKeepStr: '10', numToKeepStr: '10'))
    }
    stages
    {
        stage ('Display PATH of Jenkins')
        {
            steps
            {
                sh '''
                    echo "This is a Declarative Pipeline for building ServiceApp"
                    echo "PATH = ${PATH}"
                '''
            }
        }
        stage('Checkout the Source Code')
        {
            steps
            {
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/raambati/Jenkins_Demo.git']]])
            }
        }
        stage('Building the Sourcecode using Maven')
        {
            steps
            {
                sh 'mvn clean compile install'
            }
        }
        stage('Archive Artefact for ServiceApp')
        {
            steps
            {
                archiveArtifacts artifacts: '**/**/*.war', followSymlinks: false
            }
        }
    }
}