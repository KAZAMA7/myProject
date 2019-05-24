pipeline{

agent{
     label 'Linux'
     }
     tools{
     maven 'M2'
     }
     stages{
             stage('CheckOut'){
             steps{
               git 'https://github.com/KAZAMA7/myProject.git'
                }
                }
             stage('Maven clean'){
               steps{
                sh 'mvn clean compile'
               }
              }
             stage('test'){
               steps{ 
                sh 'mvn test'
                junit '**/target/surefire-reports/Test-8.xml'
             }
              }
             stage('Package'){
                 steps{
                  sh 'mvn package' 
                     }
                 }
            }
}
