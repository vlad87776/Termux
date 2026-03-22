# Libs для Termux (Android 15-Включая остальные!)

Эта папка содержит быстрые команды для установки популярных инструментов и библиотек в **Termux**.

> Важно: в Termux часть вещей ставится через `pkg` (системные пакеты), а часть — через `pip`/`npm`.

## 0) Базовая подготовка

```bash
pkg update -y && pkg upgrade -y
pkg install -y x11-repo
pkg install -y git curl wget unzip tar npm
pkg install -y python python-pip clang cmake make pkg-config
```

## 1) Примеры установок «от A до C»

### A — aiogram (Python)
```bash
pip install -U aiogram
```

### B — beautifulsoup4 (Python)
```bash
pip install -U beautifulsoup4
```

### C — clang (C/C++)
```bash
pkg install -y clang
```

## 2) Часто используемые пакеты

### Python/боты/веб
```bash
pip install -U aiogram aiohttp requests fastapi uvicorn
```

### Data/ML
```bash
pip install -U numpy pandas matplotlib scipy scikit-learn
```

### JS/TS
```bash
pkg install -y nodejs
npm install -g npm yarn pnpm typescript ts-node eslint
```

### Компиляторы и сборка
```bash
pkg install -y clang lld cmake make ninja pkg-config
```

### Git и SSH
```bash
pkg install -y git openssh
```

## 3) Полезная проверка

```bash
python --version
pip --version
clang --version
node --version
git --version
```

## 4) Важные заметки

- Если `pip` ругается на PEP 668, используй virtualenv:
  ```bash
  python -m venv .venv
  source .venv/bin/activate
  pip install -U pip
  ```
- Тяжёлые ML-библиотеки могут не иметь готовых колёс под Android/aarch64.
- Для некоторых GUI-инструментов нужен `x11-repo`.
