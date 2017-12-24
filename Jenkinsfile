pipeline {
    agent any

    parameters {
        choice(choices: 'RHEL\nCENTOS', description: 'What is Image Distro?', name: 'ImageDistro')
    }

    stages {
        stage("foo") {
            steps {
                echo "flag: ${params.ImageDistro}"
            }
        }
    }
}
