pipeline {
    agent any

    stages {
        stage('Cloner le dépôt') {
            steps {
                git 'https://github.com/Claudiana27/USD-s.git'
            }
        }

        stage('Déploiement local') {
            steps {
                script {
                    def targetDir = 'C:/JenkinsDeploy/USD-s'
                    bat "if not exist ${targetDir} mkdir ${targetDir}"
                    bat "xcopy *.* ${targetDir} /E /Y /I"
                }
            }
        }
    }
}
