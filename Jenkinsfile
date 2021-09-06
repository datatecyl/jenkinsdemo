pipeline {
    agent any 
    stages {
        stage('Preparation') {
            steps {
                def listAvailableServices = "Get-Service -Name '*HL*' -ErrorAction SilentlyContinue"
                def availableService = powershell(returnStdout: true, script: listAvailableServices)                
                powershell "Write-Host ${availableService}"
                powershell 'Write-Host ${availableService}'
                
                def StopService= "Stop-Service '*HL*'"
                powershell(returnStdout: false, script: StopService)                
                def waitStopService = "(Get-Service '*HL*').WaitForStatus('Stopped', '00:00:10')"
                def stopServiceResponse = powershell(returnStdout: true, script: waitStopService)
                powershell  "Write-Host ${stopServiceResponse}"
                
            }
        }
    }
}
