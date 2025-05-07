node {
   def task = [:]
   stage ('Fetch 3000 conjur credentials threads with Throttle concurrent every single build call every seconds ') {
       // Loop through list
       for (int i = 1; i <= 30; i++)
       {
           task["Task${i}"] = {
            withCredentials([conjurSecretCredential(credentialsId: 'backup-credential', variable: 'CONJUR_SECRET')]) {
                 sh 'echo $CONJUR_SECRET |base64'
 
}
            
        }
       }
  
       parallel task
   }
}
