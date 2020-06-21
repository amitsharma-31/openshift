# openshift
Openshift Important Handy CLI

| CLI Description  | CLI           |
| ---------------- | ------------- |
| Login to cluster     | $oc login -u kubeadm -p <password>  |
| Get all the nodes in a cluster     | $oc get nodes   |
| Cpu and RAM usage of nodes  | $oc adm top nodes  |
| Describe the node details   | $oc describe node my-node-name |
| Cluster version of cluster  | $oc get clusterversion |
| Cluster version of cluster details | $oc describe clusterversion |
| List of all cluster operators | $oc get clusteroperators |
| Logs of node for particular daemon (Crio in this case) for given node | $oc adm node-logs -u crio my-node-name |
| Logs of node for particular daemon (kublet in this case) for given node | $oc adm node-logs -u kublet my-node-name |  
| Journal logs for the given node | $oc adm node-logs my-node-name|
| Chroot for any node. If ctrl plane is not working <br> and your node is not ready, not able to communicate via the ctrl plane. <br> In that case you require bastion host and <br> can't rely on debug option | $oc debug node/my-node-name <br> #chroot /host <br> #systemctl is-active kubelet|
| Logs of any given pod container | $oc logs my-podname |
| Logs of any given pod container for given container <br> if pod has more than one pod | $oc logs my-podname -c my-container-name |
| Creating a pod from deployment, but running as root user <br> and thus proving the deployment references a container image | $oc debug deployment/my-deployment --as-root |
| Open a shell inside a pod to run shell | $oc rsh my-pod-name |
| Copy from local to inside container and <br> reverse the args to reverse from containers to local | $oc cp /local/path my-pod-name:/container/path |
| Creates a tcp tunnel from local port to remote port | $oc port-forward my-pod-name local-port:remote-port |
| To get your token | $oc whoami -t |
| List all events from the current project | $oc get events |
| Skopeo to validate the registry | $skopeo inspect docker://registry.access.redhat.com/rhscl/postgresq-96-rhel7:1 |
| Path variable in windows | PATH=%PATH%;C:\Users\amit7020\Documents\minikube <br> echo %PATH% |
