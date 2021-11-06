import hudson.model.*
import hudson.EnvVars
import groovy.json.JsonSlurperClassic
import groovy.json.JsonBuilder
import groovy.json.JsonOutput
import java.net.URL


node{
 stage('Checkout') {
 
 git 'https://github.com/AnjuMeleth/DCBank.git'

    }

 stage('Build') {
 dir('') {
     withMaven(
        // Maven installation declared in the Jenkins "Global Tool Configuration"
        maven: 'M3') {
            sh 'mvn clean compile'
            }
        }
    }
 stage('Test') {
 dir('') {
     withMaven(
        // Maven installation declared in the Jenkins "Global Tool Configuration"
        maven: 'M3') {
            sh 'mvn clean test'
            }
        }
    } 
stage('Package') {
 dir('') {
     withMaven(
        // Maven installation declared in the Jenkins "Global Tool Configuration"
        maven: 'M3') {
            sh 'mvn clean package'
            }
        }
    }
 }// node

