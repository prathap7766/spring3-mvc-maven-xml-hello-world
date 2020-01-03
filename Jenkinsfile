pipeline {
    agent any
    environment {
        // This can be nexus3 or nexus2
        NEXUS_VERSION = "nexus3"
        // This can be http or https
        NEXUS_PROTOCOL = "http"
        // Where your Nexus is running
        NEXUS_URL = "ec2-3-135-186-204.us-east-2.compute.amazonaws.com:8081"
        // Repository where we will upload the artifact
        NEXUS_REPOSITORY = "final_pipeline"
        // Jenkins credential id to authenticate to Nexus OSS
        NEXUS_CREDENTIAL_ID = "nexus-credentials"
    }
    stages {
        stage("clone code") {
            steps {
                script {
                    // Let's clone the source
                    git 'https://github.com/prathap7766/spring3-mvc-maven-xml-hello-world.git';
                }
            }
        }
        stage("mvn build") {
            steps {
                script {
                    // If you are using Windows then you should use "bat" step
                    // Since unit testing is out of the scope we skip them
                    //bat(/${MAVEN_HOME}\bin\mvn -Dmaven.test.failure.ignore clean package/)
                     sh "mvn package"
      
        }
            }
        }
	}
	}
