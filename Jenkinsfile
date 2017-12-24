pipeline {
    agent any

       parameters {
        // Image Destro.
        choice(choices: 'RHEL\nCentOS' , description: 'What is the Image Destro?' , name: 'ImageDestro')
        // Required RPM.
        choice(choices: 'curl\nnet-tools\nyum-utils' , description: 'Required RPM names?' , name: 'RequiredRPM')
    }

    stages {
        stage("foo") {
            steps {
                echo "flag: ${params.ImageDestro}"
                sh "echo ${params.RequiredRPM}"
            }
        }
    }
}