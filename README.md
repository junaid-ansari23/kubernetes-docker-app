# kubernetes-docker-app
A sample application to show how to build and deploy an application on kubernetes cluster. 
I have used the openshift container plateform for deploying ang running this application. You can check the kubernetes 
config and deployment files under keubernetes folder.Openshift provies a CLI to interact with cluster.
I have also included the commands to create deloyment config,service and routes.

Stesp for build and deployment
1. Run maven build and create a application jar
2. Run docker build
3. Run docker image and test application
4. Push docker image to your docker container repository and use the same in deployment-service.yml config files in project/kubernetes.
Running application on kubernetes cluster. I have used openshift and its CLI for creating deployment and service.
1. Logging to cluster and go to openshift project/namespace where you want to run this application.
2. Create deployment and service (both are part of single yml)
oc create -f deployment-service.yml
3. Create route
oc create -f app-route.yml
If all good,application should be accessible fron route/url provided in app-route.yml, host- http://bootapp.demo.com

