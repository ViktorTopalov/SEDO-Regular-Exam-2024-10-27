pipeline {
    agent any 
    stages {
        stage('Restore dependencies') { 
            steps {
                bat 'dotnet restore'
            }
        }
        stage('Built project') { 
            steps {
                bat 'dotnet build --no-restore' 
            }
        }
        stage('Run  tests') { 
            steps {
                bat 'dotnet test --no-build --verbosity normal' 
            }
        }
    }
}