pipeline {
    agent any

    parameters {
        choice(choices: 'RHEL\CENTOS', description: 'What is Image Distro?', name: 'ImageDistro')
    }

    stages {
        stage("foo") {
            steps {
                echo "flag: ${params.ImageDistro}"
            }
        }
    }
}
