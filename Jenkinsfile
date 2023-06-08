pipeline {
    agent any

    stages {
        stage('Run Tests') {
            steps {
                // Run Selenium tests using Selenium Side Runner
                // Replace the command and parameters as per your setup
                sh 'selenium-side-runner -c "goog:chromeOptions.args=[--headless,--nogpu, --no-sandbox, --disable-dev-shm-usage,--remote-debugging-port=9222, --disable-extensions, --processes=1 ] browserName=chrome" *.side  --output-directory=results'
            }
        }
    }
    post { 
        always { 
            cleanWs()
        }
    }
}
