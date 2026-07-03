pipeline {
    agent any;
        stages{
            stage("checkout"){
                steps{
                    echo "git clone"
                }
            }
            stage("build"){
                steps{
                    echo "build stage"
                    sh "docker build -t django-todo ."
                }
            }
            stage("test"){
                steps{
                    echo "test stage"
                    sh "docker run -d -p 8000:8000 --name Django-todo django-todo:latest "
                }
            }
            stage("deploy"){
                steps{
                    echo "deploy stage"
                }
            }
        }
}    
