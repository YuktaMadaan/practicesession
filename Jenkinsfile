pipeline {
    agent any

    tools {
        maven 'Maven3'
        jdk 'JDK25'
    }

    stages {

        stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/your-username/your-repo.git'
            }
        }

        stage('1. Validate') {
            steps {
                bat 'mvn validate'
            }
        }

        stage('2. Compile') {
            steps {
                bat 'mvn compile'
            }
        }

        stage('3. Test') {
            steps {
                bat 'mvn test'
            }
        }

        stage('4. Package') {
            steps {
                bat 'mvn package'
            }
        }

        stage('5. Verify') {
            steps {
                bat 'mvn verify'
            }
        }

        stage('6. Install') {
            steps {
                bat 'mvn install'
            }
        }

        stage('7. Deploy') {
            steps {
                bat 'mvn deploy'
            }
        }

        stage('8. Clean') {
            steps {
                bat 'mvn clean'
            }
        }

        stage('9. Site') {
            steps {
                bat 'mvn site'
            }
        }
    }

    post {
        success {
            echo "✅ Build completed successfully with all 9 Maven goals!"
        }
        failure {
            echo "❌ Build failed! Check logs for errors."
        }
    }
}
