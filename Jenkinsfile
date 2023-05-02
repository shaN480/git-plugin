#!/usr/bin/env groovy
pipeline {
    agent any
   
    
    stages {
        
        stage('Detect language') {
            steps {
                step([$class: 'LanguageDetector', personalToken: 'java', repoURL: 'https://github.com/oken4567/tte' ])
            }
            
        
        }
        
    }
}
/* `buildPlugin` step provided by: https://github.com/jenkins-infra/pipeline-library */
buildPlugin(
  // Container agents start faster and are easier to administer
  useContainerAgent: true,
  // Do not stop parallel tests on first failure
  failFast: false,
  // Test Java 11 with a recent LTS, Java 17 even more recent
  configurations: [
    [platform: 'linux',   jdk: '11'], // Linux first for coverage report on ci.jenkins.io
    [platform: 'windows', jdk: '17', jenkins: '2.389']
  ]
)
