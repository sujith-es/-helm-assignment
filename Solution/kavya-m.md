# EKS Workshop Helm Chart

This repository contains a Helm chart for the UST Workshop demo application.


## Create Secret
---------
Below is the empty `secret.yaml` file. Add the Helm code to generate secret. The secret should be base 64 encoded and quotes added.

![Alt text](/images/secret-file-kavyam.png?raw=true "Title")

Add the RabbitMQ secret in `values.yaml`

![Alt text](/images/rabbitmq-secret-kavyam.png?raw=true "Title")

<b>The final secret should be as below</b>. Use Dry run commanda below to get the final yaml to verify.

![Alt text](/images/secret-solution-kavyam.png?raw=true "Title")

---------

## Fix all the lint errors
```
eksdemo> helm lint .
==> Linting .
[INFO] Chart.yaml: icon is recommended
[ERROR] templates/: parse error at (eksdemo/templates/deployment/frontend.yaml:9): function "XXXXXXXXXXXXXXXXXXX" not defined

Error: 1 chart(s) linted, 1 chart(s) failed
```
---------
## Generate dry run YAML.

Commit code and inform Sujith for review. Add your name in post-fix `yourname-workshop`

```
 helm install sujith-workshop . --dry-run > dryruns/sujith.yaml
```
