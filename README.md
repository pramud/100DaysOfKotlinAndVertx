# Day #2

 common pattern throughout Vert.x APIs <b> Fluent API </b> - A fluent API is where multiple methods calls can be chained together. 
 
 * With the code we have till now if we try to create a verticle and deploy it we will get an error "Calls to static methods in Java interfaces are prohibited in JVM target 1.6. Recompile with '-jvm-target 1.8'"
 * to fix this adding the following in build.gradle
 
 compileKotlin {
    kotlinOptions.jvmTarget = "1.8"
}

compileTestKotlin {
    kotlinOptions.jvmTarget = "1.8"
}

* Creating and deploying first verticle

Creating a verticle:
 1. Have to Extend AbstractVerticle </br>
 2. Kotlin - extending a class 
  class MyVerticle : AbstractVerticle()
