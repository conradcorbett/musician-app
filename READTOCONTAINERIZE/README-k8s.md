Follow these steps to deploy the containerized app on Karbon. First deploy your Karbon cluster.

Setup kubectl on a machine that has access to the karbon cluster, then copy the deployment.yaml file to that machine. Setup kubectl by using the KUBECONFIG file provided by Karbon. You can also SSH to the master node by using the SSH keys provided in Karbon if needed.

Some useful kubectl commands

    # kubectl get pods
    # kubectl get services
    # kubectl get pods -o wide

Create the deployment
    # kubectl apply -f deployment.yaml

Check the application is reachable on the internal IP from the master node using curl.
    
    # kubectl get pods -o wide
    From master node:
    # curl http://.172.20.1.13:3001
    # curl -I http://.172.20.1.13:3001

Check the application is reachable from the NodePort IP.

    # kubectl get services
    From master node:
    # curl -I http://172.19.74.91:80

Connect to the app using any of the node IPs on the NodePort. From browser hit
http://10.38.16.50:30685/

http://10.38.16.52:30685/

http://10.38.16.57:30685/

