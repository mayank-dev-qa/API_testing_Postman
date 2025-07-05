
pipeline
         {
 
 agent any
 
 stages {
        
        stage("clone git repository"){
                 steps{

            git url: "https://github.com/mayank-dev-qa/API_testing_Postman"
                 }
        }

        stage("Install Newman"){
                 steps{

            bat 'npm install -g newman newman-reporter-html'
                 }
        }

        stage("Run newman test"){
            
            bat 'newman run "Postman collection/API Testing Project.postman_collection.json" -r cli,html --reporter-html-export result.html'
        }
        stage("Archive artifacts"){

           steps{
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
        post {
            always{
                  echo "Pipeline execution completed successfully!!!!"
            }
        }

 }

}
