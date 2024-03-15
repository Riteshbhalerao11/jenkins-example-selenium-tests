pipeline {
    agent any
    stages {
        stage('Verify browsers are installed') {
            steps {
                powershell 'Get-Item "C:\\Program Files\\Google\\Chrome\\Application\\chrome.exe" | Select-Object -ExpandProperty VersionInfo | Select-Object -ExpandProperty ProductVersion'
            }
        }
        stage('Run Tests') {
            steps {
                bat 'mvnw.cmd clean test'
            }
        }
    }
}
