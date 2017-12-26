pipeline {
    agent any
    parameters {
        // Image Destro.
        choice(choices: 'centos7:latest\nrhel7:latest' , description: 'What is the Image Version?' , name: 'ImageVersion')
        // Required RPM.
        booleanParam(defaultValue: false, description: 'Select if "curl" is required inside the Image.', name: 'curl')
        booleanParam(defaultValue: false, description: 'Select if "net-tools" is required inside the Image.', name: 'net-tools')
        booleanParam(defaultValue: false, description: 'Select if "bind-utils" is required inside the Image.', name: 'bind-utils')
        booleanParam(defaultValue: false, description: 'Select if "bind-utils" is required inside the Image.', name: 'coreutils')
    }
     stages {
        stage ('Main Stage') {
            steps {
                script {
                    if (params.curl == true) {
                        stage ('Stage 1') {
                            sh "echo 'RUN yum install -y curl >> Dockerfile'"
                        }
                    }
                    if (env.curl == 'false') {
                        stage ('Stage 2') {
                            sh 'echo Stage 2'
                        }
                    }
                }
            }
        }
    }
}