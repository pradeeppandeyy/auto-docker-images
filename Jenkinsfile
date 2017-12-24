pipeline {
    agent any

        parameters([choice(choices: ['RHEL', 'CentOS'], description: 'What is the Image Destro?', name: 'ImageDestro'), booleanParam(defaultValue: false, description: 'Select if "curl" is required inside the Image.', name: 'curl'), booleanParam(defaultValue: false, description: 'Select if "net-tools" is required inside the Image.', name: 'net-tools'), booleanParam(defaultValue: false, description: 'Select if "bind-utils" is required inside the Image.', name: 'bind-utils')])
    
    stages {
        stage("foo") {
            steps {
                echo "flag: ${params.ImageDestro}"
                sh "echo ${params.RequiredRPM}"
            }
        }
    }
}