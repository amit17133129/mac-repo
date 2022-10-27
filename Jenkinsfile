pipeline {
    agent any
    stages {
        stage('Installation of Apache Server') {
            steps {
                sh 'sudo yum install httpd -y'
            }
        }
        stage('Creating the file') {
            steps {
                sh 'sudo echo "Changing the content on the github !!" > index.html'
                sh 'sudo cp ./index.html /var/www/html/'
            }
        }
        stage('Starting the apache server') {
            steps {
                sh 'sudo systemctl start httpd'
            }
        }
    }

}
