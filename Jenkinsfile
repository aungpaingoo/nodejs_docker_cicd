pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                // Checkout code from Git repository using SSH
                git credentialsId: '1', url: 'git@github.com:aungpaingoo/nodejs_sample.git'
                // Save the pulled code if necessary
                // (you might need additional steps here depending on your requirements)
            }
            post {
                success {
                    echo 'Code pulled and saved successfully'
                }
            }
        }
        
        stage('Deploy') {
            steps {
                // Copy code to /home/myfolder
                sh 'cp -r * /home/myfolder'
                // You can add more deployment steps here if needed
            }
            post {
                success {
                    echo 'Code deployed successfully to /home/myfolder'
                }
            }
        }
    }
}

