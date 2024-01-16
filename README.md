This is a local helm chart repo for ArgoCD local repositorie of Helm app and short how to commands

Add and download locally a chart and Untar 

    helm pull https://charts.bitnami.com/bitnami/mysql-9.16.2.tgz --untar=true

List the charts

     helm list
Update

     helm update
     
Create a template for direct kubernetes deployment

    helm template msqltest ./mysql --values=./mysql/values.yaml > msql_test.yaml 
 
Apply to kubernetes

    kubectl apply -f msql_test.yaml
  
Delete from Kubernetes

    kubectl delete -f msql_test.yaml
