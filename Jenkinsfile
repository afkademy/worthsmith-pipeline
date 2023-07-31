pipeline {
    agent any 

    stages {
        stage ('Build') {
            parallel(
                "API pipeline": {
                    build(job: 'api-pipeline', file: 'api-jenkinsfile.groovy')
                },
                "Web pipeline": {
                    build(job: 'web-pipeline', file: 'web-jenkinsfile.groovy')
                }
            )
        }
    }
}