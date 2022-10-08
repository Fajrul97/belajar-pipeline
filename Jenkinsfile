pipeline {

        agent any

        stages {

                stage('build') {

                        steps {

                                sh 'docker build -t try-pipeline'
                        }
                }

                stage('run') {

                        steps {

                                sh 'docker run --name try-pipeline -dp 5000:80 try-pipeline'
                        }

                }

        }

}