pipeline {
    agent any

    environment {
        SONAR_SCANNER_HOME = 'C:\\sonar-scanner-5.0.1.3006-windows\\bin'
        SONAR_HOST_URL = 'http://localhost:9000'
        SONAR_PROJECT_KEY = 'abdirahim1'
        SONAR_LOGIN = 'sqa_5fcffb11490f4caaaa5e7ba6795db79e73a3691f'
    }

    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/abdirahim888/FA.git'
            }
        }

        stage('SonarQube Analysis') {
            steps {
                withSonarQubeEnv('abdirahim2') {
 bat "C:\\sonar-scanner-5.0.1.3006-windows\\bin\\sonar-scanner -Dsonar.projectKey=abdirahim1 -Dsonar.sources=fg\\src -Dsonar.host.url=http://localhost:9000 -Dsonar.login=sqa_5fcffb11490f4caaaa5e7ba6795db79e73a3691f"               
              }
            }
        }
    }
}
