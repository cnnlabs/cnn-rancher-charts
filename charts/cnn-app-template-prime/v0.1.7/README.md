## What is this for?

This chart is meant to stub out `deployment`, `service` and `ingress` objects in a specific namespace. It will automatically create the `ingress` object with the needed annotations for use with the `alb-ingress` controller. Additionally, you need to set the `ingress.type` to either `internal` or `external` to decide if the ALB will be available only inside the Turner network or on the public internet.
