## What is this for?

This chart is meant to stub out `deployment`, `service` and `ingress` objects in a specific namespace. It will automatically create the `ingress` object with the needed annotations for use with the `alb-ingress` controller. Additionally, you need to set the `ingress.type` to either `internal` or `external` to decide if the ALB will be available only inside the Turner network or on the public internet.

## Usage

You _must_ define `namespace` and `ingress.type` at runtime, as there are no assigned defaults.

Example:
```
 ➜ helm install  . --namespace=whiteboard-nonprod --set ingress.type=internal
```
This will create an internally available load balancer in the namespace `whiteboard-nonprod` with the host `whiteboard-nonprod-internal.cnnio.net`.

## Initilizing an ALB and deployment for dedicated use

The syntax is exactly the same, but you'll need to add two additional flags: `--set deployment.name=<deployment name here>` and `--set deploymet.port=<deployment port>`. You can also use `--set image.url=<image url>` to start with your own image.

Example:
```
 ➜ helm install . --namespace=web-product-prod --set ingress.type=internal --set deployment.name=awesome-web-app --set deployment.port=80
```
