# GiggleViewRecorder
View Recorder support for Android 21+

##Gradle

```groovy
repositories{
    mavenCentral()
}

dependencies{
    compile 'az.giggle:giggleviewrecorder:1.0.0'
}
```

### Add Application Class to Manifest
    <application
        android:name="az.giggle.giggleviewrecorder.manager.BaseApplication"
        ......... />

### Record view
    CaptureHelper captureHelper = new CaptureHelper(this);
    RecorderSettings recorderSettings = new RecorderSettings(view);
    recorderSettings.setWithDuration(true);
    recorderSettings.setDuration(10);

    captureHelper.startRecordView(getApplication(), recorderSettings, new RecordingSession.Listener() {
    
                        @Override
                        public void onStart() {}

                        @Override
                        public void onStop() {}

                        @Override
                        public void onError(String error) {}

                        @Override
                        public void onEnd(String path) {}
                        
                    });

##Thanks
*   [Telecine](https://github.com/JakeWharton/Telecine)

License
-------

    Copyright 2016 Emil Valiyev

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.

### Support:

If you want the good work to continue please support us on

* [PAYPAL](https://www.paypal.me/ishandutta2007)
* [BITCOIN ADDRESS: 3LZazKXG18Hxa3LLNAeKYZNtLzCxpv1LyD](https://www.coinbase.com/join/5a8e4a045b02c403bc3a9c0c)
