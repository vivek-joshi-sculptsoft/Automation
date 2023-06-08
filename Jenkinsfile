pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout your source code from version control
                // Replace the repository URL and credentials as needed
                git 'https://github.com/Isarlevels/Automation.git'
            }
        }



        stage('Run Tests') {
            steps {
                // Run Selenium tests using Selenium Side Runner
                // Replace the command and parameters as per your setup
                sh 'selenium-side-runner -c "goog:chromeOptions.args=[--headless,--nogpu] browserName=chrome" *.side  --output-directory=results'
            }
        }
    }


}
