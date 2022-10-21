# Stress base to run random stress tests

## Configuration

To run test edit files in commands folder:

iteration_interval_seconds: contains a number of seconds between each loop in application container
stress_cmd: contains a script to be run on application container. This script is executed at each loop iteration
stress_init_cmd: script to be run in init container

## Usage

###  Modifying files in base dir
This test suite is packaged using kustomize.
If you're not familiar or does not want to use this template in another kustomize instanciation, modify files according your needs then run follogin command to deploy:
~~~
kubectl apply -k base/
~~~

To delete creates resources:
~~~
kubectl delte -k base/
~~~

### Using as kustomize template

This template can be used through kustomize to adapt it at your needs.
To call id add `- {PAT_TO_BASE_DIR}/` in you kustomization.yaml file then tune resources as needed.

A sample is available in *java-app-mimic* directory.
