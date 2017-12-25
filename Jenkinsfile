pipeline {
    agent any

       parameters {
        // Image Destro.
        choice(choices: 'centos7:latest\nrel7:latest' , description: 'What is the Image Version?' , name: 'ImageVersion')
        // Required RPM.
        booleanParam(defaultValue: false, description: 'Select if "curl" is required inside the Image.', name: 'curl')
        booleanParam(defaultValue: false, description: 'Select if "net-tools" is required inside the Image.', name: 'net-tools')
        booleanParam(defaultValue: false, description: 'Select if "bind-utils" is required inside the Image.', name: 'bind-utils')
    }

    stages {
        stage("Build") {
            steps {
                script {
 //                   sh "echo "FROM env.ImageVersion"
                    if (env.curl == 'true')  {
                        sh "echo "yum install -y curl" >> Dockerfile"
                        }
 //                   if (env.net-tools == 'true')  {
 //                       sh "echo "yum install -y net-tools" >> Dockerfile"
 //                       }
//                    if (env.bind-utils == 'true')  {
//                        sh "echo "yum install -y bind-utils" >> Dockerfile"
//                        }
//                    else {
//                        echo 'Please select at least one package.'
 //                   }
                }
            }
        }   
    }
}