# k8s Test

Create x number of services

```shell
git clone git@github.com:kmassada/k8s-test.git
cd k8s-test
find . -name *.yaml -exec kubectl apply -f {} \;

kubectl get svc -w

find ./kubernetes/services -name *.yaml -exec kubectl delete -f {} \;
find ./kubernetes/deployments -name *.yaml -exec kubectl delete -f {} \;
```