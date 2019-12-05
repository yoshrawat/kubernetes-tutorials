# kubernetes-yaml
Kubernetes - Quick Command Reference 2

##kubectl describe pod <name of pod>
(Section 5): gives full information about the specified pod

##kubectl exec –it <pod name> <command>
(Section 5): execute the specified command in the pod’s container.
Doesn’t work well in Cygwin.

##kubectl get (pod | po | service | svc | rs | replicaset | deployment |
deploy)
(Section 6): get all pods or services. Later in the course, replicasets and
deployments.

##kubectl get po --show-labels
(Section 6): get all pods and their labels

##kubectl get po --show-labels -l {name}={value}
(Section 6): get all pods matching the specified name:value pair

##kubectl delete po <pod name>
(Section 8): delete the named pod. Can also delete svc, rs, deploy
##kubectl delete po --all
(Section 8): delete all pods (also svc, rs, deploy)

#Deployment Management

##kubectl rollout status deploy <name of deployment>
(Section 9): get the status of the named deployment

##kubectl rollout history deploy <name of deployment>
(Section 9): get the previous versions of the deployment

##kubectl rollout undo deploy <name of deployment>
(Section 9): go back one version in the deployment. Also optionally --
to-revision=<revision number>
We recommend this is used only in stressful emergency situations! Your
YAML will now be out of date with the live deployment