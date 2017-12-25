pipeline {
    agent any

       parameters {
        // Image Destro.
        choice(choices: 'RHEL\nCentOS' , description: 'What is the Image Destro?' , name: 'ImageDestro')
        // Required RPM.
        booleanParam(defaultValue: false, description: 'Select if "curl" is required inside the Image.', name: 'curl')
        booleanParam(defaultValue: false, description: 'Select if "net-tools" is required inside the Image.', name: 'net-tools')
        booleanParam(defaultValue: false, description: 'Select if "bind-utils" is required inside the Image.', name: 'bind-utils')
    }

    stages {
        stage("Build") {
            steps {
                script {
                    if (env.curl == 'true')  {
                        echo "yum install curl -y >> Dockerfile"
                        docker built -t centos7:v1 .
                        }
                    }
                }   
            }
        }
    }