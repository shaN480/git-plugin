pipeline {
    agent any
   
    
    stages {
        
        stage('Detect language') {
            steps {
                step([$class: 'LanguageDetector', personalToken:'use', repoURL: 'https://github.com/shaN480/git-plugin' ])
            }
            
        
        }
        
    }
}
