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
| Chroot for any node. If ctrl plane is not working <br> and your node is not ready, not able to communicate via the ctrl plane. In that <br> case you require bastion host and can't rely on debug option | $oc debug node/my-node-name <br> #chroot /host <br> #systemctl is-active kubelet|
