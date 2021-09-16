pipeline {
    agent any
    
    triggers {
        cron('TZ=Europe/Berlin\n* * * * *')
    }
    
    stages {
        stage('stage 1') {
            steps {
                script {
                    def now = new Date()
                    println 'triggered: ' + now.format("yyMMdd.HHmm", TimeZone.getTimeZone('UTC'))
                }
            }
        }
    }
}
