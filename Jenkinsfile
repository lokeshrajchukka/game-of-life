node('JDK8'){
    stage('Source Code'){
        git branch: 'sprint1_develop', url: 'https://github.com/lokeshrajchukka/game-of-life.git'
    }

    stage('Build the code'){
        sh 'mvn package'
    }

    stage('Archiving the test results'){
        junit testResults: '**/surefire-reports/*.xml'
        archiveArtifacts artifacts: '**/*.war', followSymlinks: false
    }
}