# Troubleshooting

Используйте диагностику, не удаляя cluster или PVC при первой ошибке.

```bash
kubectl get nodes
kubectl -n kubernetes-todo get pods,services,pvc,jobs
kubectl -n kubernetes-todo describe pod POD_NAME
kubectl -n kubernetes-todo logs POD_NAME --previous
kubectl -n kubernetes-todo get events --sort-by=.lastTimestamp
```

- `ImagePullBackOff`: проверьте image name, tag, `imagePullPolicy` и загрузку
  local image в kind/Minikube.
- `CrashLoopBackOff`: проверьте logs, command, environment variables и Secret.
- `Pending`: проверьте events, PVC, storage class и resources.
- Service без endpoints: сравните selector Service и labels Pod.
- Backend не видит database: проверьте service DNS, port, Secret и NetworkPolicy.
- Frontend не видит backend: проверьте Nginx proxy и Kubernetes Service name.
- Job падает: прочитайте Job Pod logs и проверьте Alembic configuration.

При обращении за помощью пришлите команду, полный текст ошибки без secrets и уже
выполненные проверки.
