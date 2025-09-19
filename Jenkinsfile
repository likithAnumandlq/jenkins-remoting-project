pipeline {
    // This directive tells Jenkins to find a remote agent with the label 'my-remote-agent'
    // and run all the steps on that machine.
    agent { label 'my-remote-agent' }

    stages {
        stage('Checkout Code on Agent') {
            steps {
                echo 'Step 1: Checking out source code on the remote agent...'
            }
        }
        stage('Build and Test on Agent') {
            steps {
                echo "Step 2: Running build and test commands on the remote agent..."
                // This is a simple Linux command to prove it's running on the agent
                sh 'echo "--- Agent System Info ---"'
                sh 'uname -a'
                sh 'echo "-------------------------"'
            }
        }
        stage('Deploy from Agent') {
            steps {
                echo 'Step 3: Deploying the application from the remote agent...'
            }
        }
    }
    post {
        success {
            echo 'Pipeline completed successfully on the remote agent!'
        }
    }
}
