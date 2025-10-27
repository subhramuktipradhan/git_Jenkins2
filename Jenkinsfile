pipeline{
    agent any
    enviroment{
        python='C:\\Users\\Subhra\\AppData\\Local\\Programs\\Python\\Python314\\python.exe'
    }
    stages{
        stage("checkout code"){
            checkout scm

        }
        stage("extract data"){
            bat "${env.python} extract.py"


        }
    }
    post{
        sucess{
            echo "sucess.."

        }
        failure{
            echo "failure"

        }
        always{
            echo "always"

        }
    }
}