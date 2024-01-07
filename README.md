# Manifesty Kubernetes dla cloud-app
To repozytorium zawiera pliki manifestów Kubernetes odpowiedzialnych za prawidłowe uruchomienie aplikacji z repozytorium [cloud_z2_source](https://github.com/pawelp29/cloud_z2_source).

## Pierwsze uruchomienie systemu
W celu pierwszego uruchomienia systemu wykonano następujące polecenia:

```
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
kubectl apply -f ingress.yaml
kubectl apply -f operator.yaml
```

W celu sprawdzenia poprawności działania użyto polecenia `curl`:

```
curl http://zad2.lab
```

Poprawność utworzenia środowiska sprawdzono także za pomocą poleceń `kubectl`:

```
kubectl get deploy cloud-app
kubectl describe deploy cloud-app
```

![Pierwsze uruchomienie](./first_run.png)

![Sprawdzenie obiektu deployment](./describe.png)

![Pierwsze sprawdzenie zdarzeń](./events_1.png)

