## CNN App Temlpate

### What is this for?

This chart is intended for bootstrapping a new production environment for your app. You can either link it to an existing deployment and just have this chart create a dedicated load balancer, or you can create a new deployment from scratch.

### Usage

Enter the `deployment` (aka `workload`) name in the `Name` field below. If you choose to _not_ create a new deployment, you must enter the name of the existing deployment and ensure that you deploy this chart into the namespace where the existing deployment is running.

If you choose to create a new deployment, ensure that a deployment with the same name isn't already running the namespace you choose.

Regardless of your selection, bes sure to select an existing namespace by clicking `customize` to the right of `This application will be deployed into the cnn-app-template namespace`, then `use an existing namespace` and selecting the proper prod namespace for your deployment.
