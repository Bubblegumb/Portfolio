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
                echo "Test file generation."
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
        // stage("Code Analysis") {
        //     steps {
        //         echo "Integrate a code analysis tool to analyze the code and ensure it meets industry standards."
        //         echo "SonarQube can be useful in this case for continuous inspection of code quality and security."
        //     }
        // }
        // stage("Deploy") {
        //     steps {
        //         echo "Perform a security scan on the code using a tool to identify any vulnerabilities."
        //         echo "ZAP (Zed Attack Proxy) is a popular open-source web application security scanner."
        //     }
        //     post {
        //         success {
        //             emailext(
        //                 attachLog: true,
        //                 to: "artmania260@gmail.com",
        //                 subject: "Build Status Email",
        //                 body: "The file is safe to use.",
                        
        //             )
        //         }
        //         failure {
        //             emailext(
        //                 attachLog: true,
        //                 to: "artmania260@gmail.com",
        //                 subject: "Build Status Email",
        //                 body: "Security issues found in the files presented.",
        //             )
        //         }
        //     }
        // }
        // stage("Release") {
        //     steps {
        //         echo "Deploy the application to a production server."
        //         echo "Azure is also used in this stage. Aside from that, AWS and Ansible can also be used."
        //     }
        // }
        // stage("Monitoring and Alerting") {
        //     steps {
        //         echo "Deploy the application to a production server."
        //         echo "Azure is also used in this stage. Aside from that, AWS and Ansible can also be used."
        //     }
        // }
        
    }
}

