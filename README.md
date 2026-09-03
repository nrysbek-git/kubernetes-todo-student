# Kubernetes Todo Lab — Student Starter

Промежуточный практический проект по Kubernetes для программы «DevOps с нуля до
production».

Вы получаете только application layer:

- `frontend/` — React frontend;
- `backend/` — FastAPI backend;
- `LICENSE` и `NOTICE` — информация об исходном open-source проекте;
- `ASSIGNMENT.md` — задания и критерии оценки.

В repository намеренно отсутствуют Dockerfiles, Docker Compose, Kubernetes YAML,
Helm chart, cloud infrastructure и готовые secrets. Их необходимо создать
самостоятельно.

Начните с [PREREQUISITES.md](PREREQUISITES.md), затем прочитайте
[ASSIGNMENT.md](ASSIGNMENT.md) и [GRADING_RUBRIC.md](GRADING_RUBRIC.md).

## Итог

Приложение должно запускаться:

1. на `http://localhost:8081` через Docker Compose;
2. на `http://localhost:8081` через `kubectl port-forward` из локального
   Kubernetes cluster.

Cloud account, платный domain, HTTPS и Helm для этой практики не нужны.
