# Day #1 - Setting up project

running <b>gradle init</b> in command prompt </br> and seting the values as below:
  * project type - application </br>
  * implementation language - kotlin </br>
  * split functionality across multiple sub projects - no </br>
  * build script DSL - groovy </br>
  
Adding vertx-core, vertx-web, vertx web api dependencies in build.gradle file 



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
  "class MyVerticle : AbstractVerticle()"






# Day #3

* Creating a simple HTTP Server

TODO Understand the HTTP/1.0, HTTP/1.1 and HTTP/2 protocols, websocket framesize

The default host is 0.0.0.0 which means 'listen on all available addresses' and the default port is 80.

5 lines to create a simple HTTP Server

    var server = Vertx.vertx().createHttpServer()
    server.requestHandler({req ->
        req.response().end("Hello World!")
    })
    server.listen()


* Serving a file 

 req.response().sendFile("web/${file}")
