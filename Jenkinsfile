pipeline {
    agent any

    stages {
        stage("Install Newman") {
            steps {
                bat 'npm install -g newman newman-reporter-html'
            }
        }

        stage("Run newman test") {
            steps {
                script {
                    def result = bat(script: 'newman run "Postman collection/API Testing Project.postman_collection.json" -r cli,html --reporter-html-export result.html', returnStatus: true)
                    if (result != 0) {
                        echo "Newman tests failed but continuing pipeline"
                    }
                }
            }
        }

        stage("Archive artifacts") {
            steps {
                archiveArtifacts artifacts: 'result.html', fingerprint: true
            }
        }

        stage("Publish HTML Report") {
            steps {
                publishHTML(target: [
                    allowMissing: false,
                    alwaysLinkToLastBuild: true,
                    keepAll: true,
                    reportDir: '.',
                    reportFiles: 'result.html',
                    reportName: 'Newman HTML Report'
                ])
            }
        }
    }

    post {
        always {
            echo 'Pipeline execution completed successfully!!!!'
        }
    }
}

          
  
