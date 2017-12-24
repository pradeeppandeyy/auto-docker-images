pipeline {
    agent any

       parameters {
        choice(choices: 'US-EAST-1\nUS-WEST-2', description: 'What AWS region?', name: 'region')
        // choices are newline separated
        choice(choices: 'US-EAST-1\nUS-WEST-2', description: 'What AWS region?', name: 'region')
    }

    stages {
        stage("foo") {
            steps {
                echo "flag: ${params.userFlag}"
                sh "echo ${params.region}"
            }
        }
    }
}