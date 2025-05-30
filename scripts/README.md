# 🔧 kubectl-gettop

`kubectl-gettop` — це простий Bash-плагін для Kubernetes, який дозволяє виводити статистику по CPU та памʼяті для pod'ів у зазначеному namespace.

Цей плагін створений як просте розширення `kubectl`, сумісне з будь-яким кластером (включно з K3s), і може допомогти швидко переглядати ресурсне споживання.

## 📦 Вимоги

- Bash
- `kubectl` встановлений та сконфігурований (або `k3s`)
- `metrics-server` повинен бути встановлений у кластері

## 🛠 Установка

```bash
# Копіюємо скрипт у директорію з плагінами
sudo cp kubectl-gettop /usr/local/bin/kubectl-gettop

# Робимо виконуваним
sudo chmod +x /usr/local/bin/kubectl-gettop
```

## 🚀 Приклад використання

```bash
# Отримати статистику по pod'ам у namespace default
kubectl gettop -r pod -n default

# Отримати статистику по pod'ам у вказаному namespace
kubectl gettop -r pod -n my-demo-asciiartify
```

## ⚠️  Обмеження
	•	На цей момент підтримується лише ресурс pod
	•	Для роботи потрібен встановлений metrics-server у кластері
