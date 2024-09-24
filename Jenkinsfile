pipeline {
    agent any 
    environment {
        PATH ="C:\Users\SE\apache-maven-3.9.9\bin:$PATH"
    }
    stages {
        stage("Build") {
            steps {
                echo "Test file generation."
                sh  'mvn clean package'
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
        // stage("Test") {
        //     steps {
        //         echo "Run unit tests to ensure the code functions as expected and run integration tests to ensure the different components of the application work together as expected."
        //         echo "JUnit is the popular Java framework used for unit testing and integration."
        //         echo "If you are looking for something for web development, Selenium can be useful."
        //     }
        // }
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

