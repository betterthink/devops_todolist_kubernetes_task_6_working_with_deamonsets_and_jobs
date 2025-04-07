# Django ToDo List
## Deploying manifests to cluster
1.  ```bash
    cd .infrastructure/
    ```
2. ``` bash
   kubectl apply -f daemonset.yml
   ```
3. ```bash
   kubectl aplly -f cronjob.yml
   ```
## Validation of the solution
### Daemonset:
```bash
kubectl get daemonset -n mateapp
```
### CronJob:
```bash
kubectl get cronjob -n mateapp
```
## Getting logs
```bash
kubectl get pods -n mateapp
```
### Daemonset:
```bash
kubectl logs <todoapp-server-(Daemonset)> -n mateapp
```
### CronJob:
```bash
kubectl logs <todoapp-server-(CronJob)> -n mateapp
```