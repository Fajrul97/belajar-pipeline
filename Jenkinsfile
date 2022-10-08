pipeline {

        agent any

        environment {

            DOCKER_NAME = "try-pipeline"

        }

        stages {

                stage('build') {

                        steps {

                                sh 'docker build -t ${DOCKER_NAME} .'
                        }
                }

                stage('clean up') {

                        steps {

                                sh 'docker stop ${DOCKER_NAME} || true'
                                sh 'docker rm ${DOCKER_NAME} || true'
                        }
                }

                stage('run') {

                        steps {

                                sh 'docker run --name ${DOCKER_NAME} -dp 5000:80 ${DOCKER_NAME}'
                        }

                }

        }

}