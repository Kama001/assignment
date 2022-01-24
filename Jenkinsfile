pipeline {
    agent any
    stages {
        stage('check') {
            def lastChanges
            steps {
                sh 'git log HEAD^..HEAD --pretty="%h %an - %s" > GIT_CHANGES'
                lastChanges = readFile('GIT_CHANGES')
                echo "$lastChanges"
            }
        }
    }
}
