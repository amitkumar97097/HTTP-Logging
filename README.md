HTTP logging interceptor for OkHttp2 and OkHttp3

For more information please see the website.

Download
Using OkHttp2: Download the latest JAR or grab via Maven: Maven Central Bintray



<dependency>
  <groupId>com.jleth.util</groupId>
  <artifactId>okhttp2-logging</artifactId>
  <version>1.0.1</version>
</dependency>
or Gradle:


compile 'com.jleth.util:okhttp2-logging:1.0.1'
Using OkHttp3: Download the latest JAR or grab via Maven: Maven Central Bintray


<dependency>
  <groupId>com.jleth.util</groupId>
  <artifactId>okhttp3-logging</artifactId>
  <version>1.0.2</version>
</dependency>
or Gradle:


compile 'com.jleth.util:okhttp3-logging:1.0.2'
Usage
To use the logging interceptor to the OkHttpClient in your project, do the following:

OkHttpClient.Builder builder = new OkHttpClient.Builder();
Interceptor loggingInterceptor = new LoggingInterceptorOkHttp3(new LoggingInterceptorOkHttp3.Logger() {
            @Override
            public void info(String log) {
                System.out.println(log);
            }
        });
clientBuilder.addInterceptor(loggingInterceptor);
OkHttpClient okClient = builder.build();
Snapshots of the development version are available in Sonatype's snapshots repository.

License
Copyright 2015 amitkumar97097

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
