pipeline {
  agent any
  triggers { pollSCM('H/2 * * * *') }

  stages {
    stage('Build') { steps { echo 'Build with Maven/Gradle' } }
    stage('Unit and Integration Tests') { steps { echo 'Run Jest/Mocha + integration tests' } }
    stage('Code Analysis') { steps { echo 'Run ESLint/PMD/Checkstyle' } }
    stage('Security Scan') { steps { echo 'Run OWASP Dependency-Check or Snyk' } }
    stage('Deploy to Staging') { steps { echo 'Deploy to AWS EC2 (staging)' } }
    stage('Integration Tests on Staging') { steps { echo 'Postman/Newman tests on staging' } }
    stage('Deploy to Production') { steps { echo 'Deploy to AWS EC2 (prod)' } }
  }
}
