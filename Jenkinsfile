pipeline{

    agent any
    // here any = keyword given by jenkins
    // Iany = any available server where jenkisn can run the pipeline
    // rightnow the available server the ec2 machien where jenkisn is installed
    // so any = current machine

    tools{
        maven 'mymaven'
        // here myamevn= version of the maven that we configured in tools section of Jenkins
    }
    stages{
        stage('Clone the Repo'){
            steps{
                git 'https://github.com/rakeshr6/DevOpsCodeDemo.git'
            }
        }
        stage('Compile the code'){
            steps{
                sh 'mvn compile'
                // if using windows give: bit 'mvn compile'
            }
        }
        stage('Test the code'){
            steps{
                sh 'mvn test'
                // if using windows give: bat 'mvn compile'
            }
        }
        stage('Build the code'){
            steps{
                sh 'mvn package'
                // if using windows give: bat 'mvn compile'
            }
        }
        stage('Deploy code'){

            steps{
                echo "Deploy code"
            }
        }
    }
}