## Start Minikube

Start the cluster, by running the minikube start command:

`minikube start --wait=false`{{execute}}

## Enable Dashboard

Enable the dashboard using Minikube with the command

`minikube addons enable dashboard`{{execute}}

Make the Kubernetes Dashboard available by deploying the following YAML definition. This should only be used on Katacoda.

`kubectl apply -f /opt/kubernetes-dashboard.yaml`{{execute}}

To see the progress of the Dashboard starting, watch the Pods within the kube-system namespace using

`kubectl get pods -n kubernetes-dashboard -w`{{execute}}

Once running, the URL to the dashboard is:
https://[[HOST_SUBDOMAIN]]-30000-[[KATACODA_HOST]].environments.katacoda.com/
