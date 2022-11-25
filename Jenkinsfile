pipeline{

    agent any

    stages{

        stage ('Cloning our git'){

          steps{

             git 'https://github.com/Yamato8163/INSPECTION-a_messaging_app.git'

          }

        }

        stage ('Building our image'){

          steps{

            script{

                sh 'docker build -t rahulanand04292/inspectionamessagingapp .'

                // docerImage = dock÷er.build registry + ":$BUILD_NUMBER"

            }

          }  



        }

        stage('Deploy our image') {

            steps {

                script {

                    sh 'docker login -u rahulanand04292 -p Rahul@Anand'

                    sh 'docker image push rahulanand04292/inspectionamessagingapp'

                    

                }

            }

        }

    }

}