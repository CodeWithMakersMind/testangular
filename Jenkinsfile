// pipeline {
//      agent any
//      stages {
//         stage("Install Dependencies") {
//             steps {
//                 sh "sudo npm install -g @angular/cli"
//                 sh "sudo npm install"
//             }
//         }

//         stage("Build") {
//             steps {
//                 sh "sudo ng build"
//             }
//         }

//         stage("Deploy") {
//             steps {
//                 sh "sudo rm -rf /var/www/angulartest.mmworkspace.com"
//                 sh "sudo cp -r ${WORKSPACE}/dist/ /var/www/angulartest.mmworkspace.com/"
//             }
//         }
//     }
// }

pipeline {
    agent any
    stages {
        stage("Install Dependencies") {
            steps {
                bat "npm install -g @angular/cli"
                bat "npm install"
            }
        }

        stage("Build") {
            steps {
               bat "ng serve"
            }
        }

        stage("Run Nginx") {
            steps {
                
                bat "\"C:\\Program Files\\nginx-1.27.2\\nginx.exe\""
            }
        }
    }
}









