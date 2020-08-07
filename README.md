# k8s-sharedInformers Using SharedInformerFactory
A K8s informer listens to a new Pod Creation ,Deletion and Updation.
These is a long running app which will keep on listening to the Pods events 
and will return the Pod name and namespace where the resocue is created ,deleted or updated.

podsevents/webserver2

These application is safe to use as it will notgoing to call the api server again an again
instead when there is a new resource in the api server.Also the information is stored in the SharedInformers cache.

These app can be exteded to any kind of action or automation based on any change in K8s regards to Pod,NS,Nodes and etc.
