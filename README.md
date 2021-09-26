# recruitee

```
sudo -E kubectl version --short

sudo -E /usr/local/bin/helm repo add rasa-x https://rasahq.github.io/rasa-x-helm

sudo -E /usr/local/bin/helm install \
    --namespace recruitee \
    --values values.yml \
    rasa-x-recruitee-one \
    rasa-x/rasa-x

sudo -E /usr/local/bin/helm --namespace recruitee list

sudo -E /usr/local/bin/helm upgrade \
    --namespace recruitee \
    --values values.yml \
    rasa-x-recruitee-one \
    rasa-x/rasa-x

sudo -E kubectl --namespace recruitee get pods
sudo -E kubectl --namespace recruitee get deployments
sudo -E kubectl --namespace recruitee get services
```

```
sudo -E kubectl --namespace recruitee create secret generic recruitee-postgres
sudo -E kubectl --namespace recruitee edit secrets recruitee-postgres

sudo -E /usr/local/bin/helm delete --namespace recruitee rasa-x-recruitee-one

sudo -E kubectl -n recruitee logs -f
```
