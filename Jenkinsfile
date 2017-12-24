pipeline {
    agent any

    env.RELEASE_SCOPE = input message: 'User input required', ok: 'Release!',
                            parameters: [choice(name: 'RELEASE_SCOPE', choices: 'patch\nminor\nmajor', description: 'What is the release scope?')]
                            
    stages {
        stage("foo") {
            steps {
                script {
                }
                echo "${env.RELEASE_SCOPE}"
            }
        }
    }
}