pipeline {
    agent any 

    stages {
        stage ('Build') {
            parallel{
                stage("API Pipeline") {
                    steps {
                        build(job: 'api-pipeline', parameters: [file('api-jenkinsfile.groovy')])
                    }
                }
                
                stage("Web pipeline") {
                    steps {
                        build(job: 'web-pipeline', parameters: [file('web-jenkinsfile.groovy')])
                    }
                }
            }
        }
    }
}
