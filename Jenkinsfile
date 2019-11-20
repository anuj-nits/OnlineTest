#!/usr/bin/env groovy
import hudson.model.*
import hudson.EnvVars
import java.net.URL

node{
    stage('Git Checkout'){
        git 'https://github.com/anuj-nits/OnlineTest.git'
    }
    stage('Compile App'){
            withMaven(maven:'Maven 3'){
            sh 'mvn compile'
        }
    }
        stage('Test App'){
            withMaven(maven:'Maven 3'){
            sh 'mvn test'
        }
    }
    stage('Package App'){
            withMaven(maven:'Maven 3'){
            sh 'mvn package'
        }
    }
}
