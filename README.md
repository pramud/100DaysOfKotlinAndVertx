# 100 Days Of Kotlin And Vertx

# Day #1 - Setting up project

running <b>gradle init</b> in command prompt </br> and seting the values as below:
  * project type - application </br>
  * implementation language - kotlin </br>
  * split functionality across multiple sub projects - no </br>
  * build script DSL - groovy </br>
  
Adding vertx-core, vertx-web, vertx web api dependencies in build.gradle file 

Creating a verticle 
 * Have to Extend AbstractVerticle
 Kotlin 
  extending a class 
  class MyVerticle : AbstractVerticle()
