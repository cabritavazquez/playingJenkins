// Declarative Pipeline
Pipeline{
    agent any
    environment{
        MY_VERSION_VAR = "1.0.0"
    }
    stages{
        stage("init"){
            steps{
                echo "init"
            }
        }
        stage("build dev"){
            options{
                ansiColor("xterm")
            }
            when{
                branch "dev"
            }
            steps{
                echo "build your nice project with version ${MY_VERSION_VAR}"
            }
        }
        stage("build master"){
            when{
                branch "master"
            }
            steps{
                sh "build your nice project!"
            }
        }
        stage("push"){
            options{
                timeout(time: 5, unit: "SECONDS")
            }
            steps{
                sh "build your nice project!"
            }
        }
    }
}