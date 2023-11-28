
pipeline{
       agent {
           label {
            label "built-in"
            customWorkspace "/mnt/assign3"
           }
       }

    stages {
          stage("master deployment")
          {
            steps{
                   sh "rm -rf * "
                   sh "git clone https://github.com/Akirandive/vel-app-assign3.git"

            }
          }

           stage("server httpd configure and deployment ")
          {
            steps{
                  sh "sudo yum install httpd -y"
                  sh "sudo service httpd start "
                  sh "sudo cp -r /mnt/assign3/23Q2/index.html /var/www/html/"
                  sh "sudo chmod -R 777 /var/www/html/"
                  

               }
          }

    }
}
