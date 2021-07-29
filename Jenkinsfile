node {
    
    stage('Preparation') {
        // Get code from a GitHub repository. Explicitly kept the URL for the challenge. Else one can use a single line like 
        // checkout scm that automatically detects the SCM when one sets up MultiPipeline project. 
        git credentialsId: 'jenkins-user-github', url: 'https://github.com/Urmil-025/mobile-devops-project.git'
    }
    stage('Unit Test') {
        sh './gradlew clean runUnitTestandGenerateCSV'
    }
    stage('JUnit reports') {
        junit 'build/**/TEST-*.xml'
    }
}
