pipeline {
    agent any
    parameters {
        // Image Destro.
        choice(choices: 'centos7:latest\nrhel7:latest' , description: 'What is the Image Version?' , name: 'ImageVersion')
        // Required RPM.
        booleanParam(defaultValue: false, description: 'Select if "curl" is required inside the Image.', name: 'curl')
        booleanParam(defaultValue: false, description: 'Select if "net-tools" is required inside the Image.', name: 'net_tools')
        booleanParam(defaultValue: false, description: 'Select if "bind-utils" is required inside the Image.', name: 'bind_utils')
        booleanParam(defaultValue: false, description: 'Select if "bind-utils" is required inside the Image.', name: 'core_utils')
    }
     stages {
        stage ('Main Stage') {
            steps {
                writeFile (file: 'Dockerfile', text: 'FROM parms.ImageVersion')
                script {
                    if (params.curl == true) {
                        stage ('Stage 1') {
                            echo "This Was Successfull."
                            sh "echo -e 'RUN yum install -y curl' | tee -a Dockerfile"
                        }
                    }
                    if (params.net_tools == true) {
                        stage ('Stage 2') {
                            echo "This Was Successfull."
                            sh "echo -e 'RUN yum install -y net-tools' | tee -a Dockerfile"
                        }
                    }
                    if (params.bind_utils == true) {
                        stage ('Stage 3') {
                            echo "This Was Successfull."
                            sh "echo -e 'RUN yum install -y bind-utils' | tee -a Dockerfile"
                        }
                    }
                    if (params.core_utils == true) {
                        stage ('Stage 4') {
                            echo "This Was Successfull."
                            sh "echo -e 'RUN yum install -y core-utils' | tee -a Dockerfile"
                        }
                    }
                    
                }
            }
        }
    }
}