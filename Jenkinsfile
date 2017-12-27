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
                            echo "This Was Successfull."
                            echo -e "RUN yum install -y curl_1" | tee -a "Dockerfile"
                        }
                    }
                    if (params.curl == true) {
                        stage ('Stage 2') {
                            echo "This Was Successfull."
                            writeFile file: 'Dockerfile', text: 'RUN yum install -y curl2'
                        }
                    }
                    if (params.curl == true) {
                        stage ('Stage 3') {
                            echo "This Was Successfull."
                            writeFile file: 'Dockerfile', text: 'RUN yum install -y curl3'
                        }
                    }
                    if (params.curl == true) {
                        stage ('Stage 4') {
                            echo "This Was Successfull."
                            writeFile file: 'Dockerfile', text: 'RUN yum install -y curl4'
                        }
                    }
                    
                }
            }
        }
    }
}