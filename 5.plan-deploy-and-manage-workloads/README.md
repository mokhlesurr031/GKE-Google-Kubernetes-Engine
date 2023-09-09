# Plan, Deploy and Manage Workloads


## Node Taints 

Can assign node taines to cluster level or node pool level. 

Create cluster:

```$ gcloud container clusters create CLUSTER_NAME --num-node=1 --disk-type=pd-standard --disk-size=10 --node-taints function=research:PreferNoSchedule```

Create node pools that doesn't inherit the node-taints from origin cluster:

```$ gcloud container node-pools create NODE_POOL_NAME --num-node=1 --disk-type=pd-standard --disk-size=10 --cluster CLUSTER_NAME```

We can manually set taints to the node pool:

```$ gcloud beta container node-pools update NODE_POOL_NAME --node-taints="function=shared:NoSchedule" --cluster=CLUSTER_NAME```


