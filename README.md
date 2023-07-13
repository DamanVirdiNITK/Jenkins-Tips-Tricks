# Jenkins-Tips-Tricks</br> <B>
1.Set timeout condition for Jenkins Pipeline timeout --> timeoutPipeline.groovy</br>
2.Set timeout condition for particuar step of pipeline</br></B>

1. <B>Set timeout condition for Jenkins Pipeline timeout</B> --> timeoutPipeline.groovy</br>
    **options{ 
        timeout(time: 1,unit:'MINUTES')
    }
**</br>
After one minute complete pipeline will stop

<B>2.Set timeout condition for particuar step of pipeline</br></B>

