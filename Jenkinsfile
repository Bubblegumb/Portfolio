pipeline {
    agent any 
    tools {
        maven 'Maven'
    }
    stages {
        stage("Build") {
            steps {
                echo "Test file generation."
                bat  'mvn clean package'
            }
            post {
                success {
                    echo 'JAR file created and archived!'
                }
                failure {
                    echo 'Build failed!'
                }
            }
        }
        stage("Test") {
            steps {
                echo "Start testing"
                bat  'mvn test'
            }
            post {
                success {
                    echo 'Test successful'
                }
                failure {
                    echo 'Test failed!'
                }
            }
        }
        // stage("Sonarqube Analysis") {
        //     steps {
        //         echo "Integrate a code analysis tool to analyze the code and ensure it meets industry standards."
        //         withSonarQubeEnv(installationName: 'SonarCube') {
        //             bat 'mvn clean sonar:sonar'
        //         }
        //     }
        // }
        stage("Deploy") {
            steps {
                echo "Deploy"
            }
        }
        stage("Release") {
            steps {
                echo "Deploy the application to a production server."
            }
        }
        stage("Monitoring and Alerting") {
            steps {
                echo "Monitor the application and send alert."
            }
        }
    }
    post {
        success {
            emailext(
                attachLog: true,
                to: "artmania260@gmail.com",
                subject: "Build Status Email",
                body: "Pipeline deployed successfully.",
                
            )
        }
        failure {
            emailext(
                attachLog: true,
                to: "artmania260@gmail.com",
                subject: "Build Status Email",
                body: "Failed to deploy pipeline.",
            )
        }
    }
}

