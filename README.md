# TheHive + Cortex + Elasticsearch + Cassandra + Nginx (HTTPS)

Stack Docker com:

- TheHive 4
- Cortex
- Elasticsearch
- Cassandra
- Nginx fazendo proxy reverso + HTTPS com certificado autoassinado

Este README foi feito para facilitar a primeira instalação e os próximos deploys.

## ✅ Pré-requisitos

- Linux (testado em Ubuntu 22.04+)
- Docker
- Docker Compose v2 (`docker compose`)
- Git

Confirme:

```
docker --version
docker compose version
```

## 📥 1. Baixar o Script de Instalação

```
wget https://packages.genesissecurity.com.br/thehive/thehive_cortex.sh
chmod +x thehive_cortex.sh
./thehive_cortex.sh
```

## ♻️ 2. Atualizar API Key futuramente

```
Após criar o seu usuario e criar um usuario para integração, gere uma apikey e copie ela
Edite .env
E cole a api key em CORTEX_KEY=
docker compose restart thehive
```

## 🛠️ 3. Troubleshooting

### TheHive reiniciando
→ `.env` inválido

### Erro de index
```
rm -rf vol/thehive/index
chown -R 1000:1000 vol/thehive
chmod -R 775 vol/thehive
docker compose restart thehive
```








