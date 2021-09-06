pipeline {
    agent any 
    stages {
        stage('Preparation') {
            steps {
                script {           
                    def services = powershell(returnStdout: true, script: "Get-Service -Name '*HL7*' -ErrorAction SilentlyContinue")
                    if (services != null) {
                        def StopService= "Stop-Service '*HL*'"
                        def stopIt = powershell(returnStdout: true, script: StopService)                
                        def waitStopService = "(Get-Service '*HL*').WaitForStatus('Stopped', '00:00:10')"
                        def stopServiceResponse = powershell(returnStdout: true, script: waitStopService)
                        println stopServiceResponse
                    }
                }
            }
        }
    }
}
