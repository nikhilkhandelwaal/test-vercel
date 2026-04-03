pipeline{
    agent any
    docker {
        image 'node:18'
    }
    environment{
        VERCEL_TOKEN=credentials('VERCEL_TOKEN')
    }
    stages{
        stage('Install'){
            steps{
                sh 'npm install'
            }
        }
        stage('Test'){
            steps{
                sh "test done"
            }
        }
        stage('Build'){
            steps{
                sh 'npm run build'
            }
        }
        stage('Deploy'){
            steps{
                sh 'npx vercel --prod --yes --token=%VERCEL_TOKEN%'
            }
        }
    }
}