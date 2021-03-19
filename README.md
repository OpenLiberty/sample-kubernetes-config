# Externalizing config using MicroProfile, ConfigMaps and Secrets Kubernetes Sample

This repository contains the sample code required for the Java configuration tutorial on Kubernetes.io. The tutorial can be found here: https://kubernetes.io/docs/tutorials/configuration/configure-java-microservice/configure-java-microservice/

It has an interactive element that clones down this repository when the interactive session is started. 

## Objectives
- Create a Kubernetes ConfigMap and Secret
- Inject microservice configuration using MicroProfile Config

## What you'll learn
You will learn how and why to externalize your microservice’s configuration. Externalized configuration is useful because configuration usually changes depending on your environment. You will also learn how to configure the environment by providing required values to your application using Kubernetes. Using environment variables allows for easier deployment to different environments.

MicroProfile Config provides useful annotations that you can use to inject configured values into your code. These values can come from any config sources, such as environment variables. To learn more about MicroProfile Config, read the Configuring microservices guide.

Furthermore, you’ll learn how to set these environment variables with ConfigMaps and Secrets. These resources are provided by Kubernetes and act as a data source for your environment variables. You can use a ConfigMap or Secret to set environment variables for any number of containers.

## The Application
The two microservices you will deploy are called system and inventory. The system microservice returns the JVM system properties of the running container and it returns the pod’s name in the HTTP header making replicas easy to distinguish from each other. The inventory microservice adds the properties from the system microservice to the inventory. This demonstrates how communication can be established between pods inside a cluster.