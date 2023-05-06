pipeline {
    agent any
    tools {
        jdk "java17"   //java17 is a label which we updated in global tool configuration
        maven "maven3"
    }
    stages {
        stage("cleanup workspace") {
            steps {
                cleanWs()
            }
        }

        stage("Checkout from SCM") {
            steps {
                git branch: 'main', credentialsId: 'github', url: 'https://github.com/naresh9919/complete-prodcution-e2e-pipeline.git'
            }
        }
    }
}
