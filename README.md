# Jenkins-Tips-Tricks</br> <B>
1.Set timeout condition for Jenkins Pipeline timeout --> timeoutPipeline.groovy</br>
2.Set timeout condition for particuar stage of pipeline</br> --> timoutStageinPipelinewithAbort.txt</br>
3.Set timeout for particualr stage of pipeline but skip that stage only --> timeoutStageInPipelinewithoutAbort.txt</br>

</B>
<B>1.Set timeout condition for Jenkins Pipeline timeout</B> --> timeoutPipeline.groovy</br>
    **options{ 
        timeout(time: 1,unit:'MINUTES')
    }
**</br>
After one minute complete pipeline will stop</B></br>

<B>2.Set timeout condition for particuar stage of pipeline --> timoutStageinPipelinewithAbort.txt</br></B>
Since in the first stage, we face timout even before the stage could get completed, In stage add.  
**options {<t>
                timeout(time: 1, unit: 'HOURS')
            }**</br></br>
<B>3.Set timeout for particualr stage of pipeline but skip that stage only --> timeoutStageInPipelinewithoutAbort.txt</br></B>
Inside the steps add</br><b>
**       timeout(time: 4, unit: 'MINUTES'){
                    catchError(buildResult: 'SUCCESS', stageResult: 'FAILURE') {
                        echo 'Hello World'
                        sleep 300
                    }    
                }
         **</b></br>
