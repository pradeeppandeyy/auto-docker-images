pipeline {
    agent any

       parameters {
        // Image Destro.
        choice(choices: 'centos7:latest\nrhel7:latest' , description: 'What is the Image Version?' , name: 'ImageVersion')
        // Required RPM.
        booleanParam(defaultValue: false, description: 'Select if "curl" is required inside the Image.', name: 'curl')
        booleanParam(defaultValue: false, description: 'Select if "net-tools" is required inside the Image.', name: 'net-tools')
        booleanParam(defaultValue: false, description: 'Select if "bind-utils" is required inside the Image.', name: 'bind-utils')
    }
    stages {
        stage("Build") {
            when {
                environment name: 'curl', value: 'true'
            }
                steps {
                            stage("Build") {
            when {
                environment name: 'curl', value: 'true'
            }
                steps {
                 sh "echo FROM ${env.ImageVersion} > Dockerfile && echo yum install -y curl >> Dockerfile"   
                }
            }
                 sh "echo FROM ${env.ImageVersion} > Dockerfile && echo yum install -y curl >> Dockerfile"   
                }
            }
        }
    }




