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
                $maxTimeout = New-TimeSpan -Seconds 10
                def waitStopService = "(Get-Service '*HL*').WaitForStatus('Stopped', ${$maxTimeout})"
                def stopServiceResponse = powershell(returnStdout: true, script: waitStopService)
                powershell  "Write-Host ${stopServiceResponse}"
                
            }
        }
    }
}
