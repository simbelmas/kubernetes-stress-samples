# Stress tests with startup/liveness probes

This stress test is meant to  mimic a old fashioned java application that consumes a lot of cpu at startup and only memmemoryopry after.

## Configuration

FOr configuration details, please view README.md in base/ directory

## Usage

To deploy:
~~~
kubectl apply -k java-app-mimic/
~~~

To delete:
~~~
kubectl delete -k java-app-mimic/
~~~

This can also be used as a kustomize template.