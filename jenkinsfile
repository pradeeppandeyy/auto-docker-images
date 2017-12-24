pipeline    {
    agent   any
    stages  {
        stage('stage 1') {
                steps   {
                    echo 'this is first stage.'
                    sh 'whoami'
                    sh 'docker run hello-world'
                }
            
        }
        stage('stage 2') {
            steps   {
                echo 'this is second stage'
            }
        }
        stage('stage 3') {
            steps   {
            echo    'this is third stage'
            }
        }
        stage('stage 4') {
            steps   {
            echo    'this is fifth stage'
            }
        }
    }
}