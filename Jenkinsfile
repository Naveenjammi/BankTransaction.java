pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/your-repo/bank-transaction.git'
            }
        }

        stage('Build') {
            steps {
                sh './gradlew build' // or 'mvn clean package' if using Maven
            }
        }

        stage('Run Transaction') {
            steps {
                sh 'java -cp build/classes/java/main BankTransaction' // Adjust path based on your build setup
            }
        }
    }
}

