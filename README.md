## Kubernetes/Container Engine Visualizer

This is a simple visualizer for use with the Kubernetes API.

NB! As replicationcontroller is depricated it is replaced with deployment

### Usage:
   * First install a Kubernetes or Container Engine Cluster
   * ```git clone https://github.com/PS1c0m/gcp-live-k8s-visualizer.git```
   * ```kubectl proxy --www=path/to/gcp-live-k8s-visualizer```

That's it.  The visualizer uses labels to organize the visualization.  In particular it expects that

   * pods, replicationcontrollers, and services have a ```name``` label, and pods and their associated replication controller share the same ```name```, and
   * the pods in your cluster will have a ```uses``` label which contains a comma separated list of services that the pod uses.


   - White indicates a healthy node
   - Red indicates a non-healthy node
   - Gray indicates a running pod
   - Yellow indicates a pending pod
   - Green indicates a service
   - Blue indicates a replication controller
