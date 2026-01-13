pipeline {
    agent any

    tools {
        maven 'Maven-3.8.x'
    }

    stages {

        stage('Checkout Code') {
            steps {
                git url: 'https://github.com/YuktaMadaan/practicesession.git', branch: 'main'
            }
        }

        stage('Run 9 Maven Goals') {
            steps {
                bat """
                mvn validate
                mvn compile
                mvn test
                mvn package
                mvn verify
                mvn install
                mvn deploy
                mvn clean
                mvn site
                """
            }
        }
    }

    post {
        success {
            echo "✅ SUCCESS: All 9 Maven goals executed successfully!"
        }
        failure {
            echo "❌ FAILED: Check console output for errors."
        }
    }
}

