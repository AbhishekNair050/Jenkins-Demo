pipeline {
    agent any
    stages {
        stage('Job 1') {
            steps {
                build job: 'JOB_1', propagate: true
            }
        }
        stage('Job 2') {
            steps {
                build job: 'JOB_2', propagate: true
            }
        }
        stage('Job 3') {
            steps {
                build job: 'JOB_3', propagate: true
            }
        }
    }
}
