# k8s-sharedInformers Using SharedInformerFactory

This is a long-running app which will keep on listening to the Pods events 
and will return the Pod name and namespace where the resource is created ,deleted or updated.

e.g. Output : podsevents/webserver2
              kube-system/kiam-agent-nlqf2

This application is safe to use as it will not go to call the api server again an again
instead when there is a new resource in the api server this app will capture that event.Also, the information is stored in the SharedInformers cache.
This app can be extended to any kind of action or automation based on any change in K8s regards to Pod,NS,Nodes etc.
