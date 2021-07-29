pipeline{
    agent any
    environment{
        name = "Jenkins"
    }
    stages{
        stage("Pre defined"){
            steps{
                echo " current build number is -  $BUILD_NUMBER"
            }
        }
        stage("User defined"){
            steps{
                echo " User defined variable is - $name"
            }
        }
        stage("Declartion Types"){
             environment{
                    name = "Ansible"
                }
            steps{
                script{
                    tool="Postman"
                }
                echo "varible declared from in steps is - $tool "
                echo "varible declared from in stage of Declaration Types is - $name "
            }
        }
        stage("Retrive from Env variabes"){
            environment{
                job ="full stack developer"
            }
            steps{
                script{
                    job="java developer"
                }
                echo"job varble from script section is - $job"
                echo"job varble from environment section is - ${env.job}"
            }
        }
    }
}
