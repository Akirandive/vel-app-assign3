
pipeline{
       agent {
           label {
            label "slave-1"
            customWorkspace "/mnt/assign3"
           }
       }

    stages {
          stage("clone project")
          {
            steps{
                sh "rm -rf * "
                sh "git clone https://github.com/Akirandive/vel-app-assign3.git -b 23Q1 "

            }
          }
          stage("server httpd configure and deployment ")
          {
            steps{
                  sh"sudo yum install httpd -y"
                  sh"sudo service httpd start "
                  sh "sudo cp /mnt/assign3/vel-app-assign3/index.html /var/www/html/"
                  sh "sudo chmod -R 777 /var/www/html/"
               }
          }

    }
}
