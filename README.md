# install-guide

## Useful Links
* https://hyperledger.github.io/composer/installing/installing-index
* https://ibm-blockchain.github.io/develop/installing/installing-index
* https://ibm-blockchain.github.io/setup/
* https://ibm-blockchain.github.io/platform-deployment/
* https://www.npmjs.com/package/generator-hyperledger-composer
* https://composer-playground.mybluemix.net/login
* https://chat.hyperledger.org/channel/composer
* https://www.youtube.com/watch?v=I5xhQ0Jty6w&list=PLpryjkO3KF2w4Q68Hsi-O2t3WsbaZ-7Z3

* IBM Courses
  * https://www.coursera.org/learn/deploy-micro-kube-ibm-cloud
  * https://www.coursera.org/learn/ibm-blockchain-essentials-for-developers
  


***Gain access to your cluster***

**Prerequisites**
1. Create an IBM Account and get a Voucher from an admin.
2. Select Manage (upon right on the screen) --> Billing ang Usage --> Billing
3. Select Promocode and enter the code

If you want to generate a local Kubernetes Cluster, go to the IBM catalog (upon right on the screen) and search for Kubernetes Cluster. Once created, go to "Access" (upon left on the screen) and follow the instructions. It should be something like that:

1. Download the [IBM Cloud CLI](https://console.bluemix.net/docs/cli/reference/bluemix_cli/get_started.html#getting-started)

2. Download the [Kubernetes CLI](https://kubernetes.io/docs/tasks/tools/install-kubectl/)

3.
bx plugin install container-service -r Bluemix

4.
bx login --sso
--> it should show you a link. Copy the link and paste it in the URL. You should get the code.

5.
bx plugin show container-service

6.
bx cs cluster-config CSHack

7.
export KUBECONFIG=/Users/arman.behzadirad@ch.ibm.com/.bluemix/plugins/container-service/clusters/CSHack/kube-config-mil01-CSHack.yml
--> Use your own email, and the name of your own cluster (instead of CSHack)

8.
kubectl get nodes

9.
kubectl config view -o jsonpath='{.users[0].user.auth-provider.config.id-token}'

10.
enter token in dashboard

