# Kubernetes Infraestrutura Project 🚀

Este projeto simula um ambiente de produção com foco em infraestrutura e suporte, utilizando Kubernetes e ferramentas modernas de observabilidade e escalabilidade.

## 🎯 Objetivos

- Deploy de aplicação com alta disponibilidade
- Escalonamento automático com HPA (Horizontal Pod Autoscaler)
- Monitoramento com Prometheus e Grafana
- Coleta e visualização de logs com Loki
- Deploy automatizado com Helm

## 📦 Estrutura do Projeto

```
k8s-infra-support-project/
├── manifests/            # YAMLs de deployment, service, ingress e HPA
├── monitoring/           # Configuração Prometheus
├── logs/                 # Configuração Loki
├── helm-charts/          # Instalação via Helm
└── README.md             # Este arquivo
```

## 🚀 Como Executar Localmente

1. Instale e inicie o Minikube:
```bash
minikube start
```

2. Aplique os manifests Kubernetes:
```bash
kubectl apply -f manifests/
```

3. Instale os charts de monitoramento e logging:
```bash
helm repo add grafana https://grafana.github.io/helm-charts
helm install prom grafana/kube-prometheus-stack
helm install loki grafana/loki-stack
```

4. Atualize seu /etc/hosts com:
```bash
127.0.0.1 webapp.local
```

5. Acesse a aplicação e dashboards:
- http://webapp.local → aplicação web
- http://<grafana-url> → login: admin / senha padrão definida

## 📊 Prints Sugeridos para GitHub

- Interface do Grafana
- Escalonamento de pods via `kubectl get hpa`
- Logs visíveis no Loki

## 🤝 Contribuições
Aberto para sugestões e melhorias!

---

Feito com 💻 por Leandro Chagas – Especialista em Infraestrutura e Suporte
