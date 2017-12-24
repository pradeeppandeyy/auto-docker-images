pipeline {
    agent any

    parameters {
        choice(choices: 'RHEL\nCENTOS', description: 'What is Image Distro?', name: 'ImageDistro'),choice(choices: 'RPM\nDEB', description: 'What is  Pakage Type?', name: 'PakageType')
    }

    stages {
        stage("foo") {
            steps {
                echo "flag: ${params.ImageDistro}"
                echo "flag: ${params.PakageType}"
            }
        }
    }
}
