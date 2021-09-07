pipeline {
    agent any 
    stages {
        stage('Preparation') {
            steps {
                script {           
                    //def services = powershell(returnStdout: true, script: "Get-Service -Name '*HL7*' -ErrorAction SilentlyContinue")
                    println new File(".").absolutePath

                    /*if (services != null) {
                        def StopService= "Stop-Service '*HL7*'"
                        def stopIt = powershell(returnStdout: true, script: StopService)                
                        def waitStopService = "(Get-Service '*HL7*').WaitForStatus('Stopped', '00:00:10')"
                        try {
                            def stopServiceResponse = powershell(returnStdout: true, script: waitStopService)                            
                            println stopServiceResponse
                        } catch (Exception  e) {
                            println "stop failed."
                        }
                     */
                       /*if (services != null) {
                        def StartService= "Start-Service '*HL7*'"
                        def startIt = powershell(returnStdout: true, script: StartService)                
                        def waitStartService = "(Get-Service '*HL7*').WaitForStatus('Running', '00:00:10')"
                        try {
                            def startServiceResponse = powershell(returnStdout: true, script: waitStartService)                            
                            println startServiceResponse
                        } catch (Exception  e) {
                            println "start failed."
                        }
                    }*/
                }
            }
        }
    }
}
