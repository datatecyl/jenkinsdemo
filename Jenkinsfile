pipeline {
    agent any 
    stages {
        stage('Preparation') {
            steps {
                script {           
                    powershell "Get-Service -Name '*HL7*' -ErrorAction SilentlyContinue"
                    
/*
                    def StopService= "Stop-Service '*HL*'"
                    powershell(returnStdout: false, script: StopService)                
                    def waitStopService = "(Get-Service '*HL*').WaitForStatus('Stopped', '00:00:10')"
                    def stopServiceResponse = powershell(returnStdout: true, script: waitStopService)
  */                  
                }
            }
        }
    }
}
