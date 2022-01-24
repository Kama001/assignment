pipeline {
    agent any
    stages {
        stage('check') {
            steps {
                sh 'git log HEAD^..HEAD --pretty="%h %an - %s" > GIT_CHANGES'
                def lastChanges = readFile('GIT_CHANGES')
                echo "$lastChanges"
            }
        }
    }
}
