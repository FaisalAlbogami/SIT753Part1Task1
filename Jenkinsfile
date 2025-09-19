pipeline {
  agent any

  stages {
    stage('Build') {
      steps { echo 'Build: use npm (npm ci, npm run build) to compile/package the app.' }
    }
    stage('Unit & Integration Tests') {
      steps { echo 'Tests: run unit & integration tests (npm test) with Jest/Mocha + Supertest.' }
    }
    stage('Code Analysis') {
      steps { echo 'Code Analysis: run ESLint and/or SonarCloud via SonarScanner.' }
    }
    stage('Security Scan') {
      steps { echo 'Security: scan dependencies with npm audit or Snyk CLI (snyk test).' }
    }
    stage('Deploy to Staging') {
      steps { echo 'Deploy Staging: deploy via Docker/SSH to a staging server (e.g., EC2).' }
    }
    stage('Integration Tests on Staging') {
      steps { echo 'Staging Tests: run smoke/integration tests with Newman/Cypress.' }
    }
    stage('Deploy to Production') {
      steps { echo 'Deploy Production: promote Docker image or deploy via SSH/CD to prod EC2.' }
    }
  }

  post {
    always { echo 'Note: design-only pipeline for Part 1 - Task 1.' }
  }
}
