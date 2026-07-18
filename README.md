# 🍝 FusionBite - Self-Ordering System

Un moderno sistema di self-ordering per ristoranti fusion emiliano-romagnoli. Combina piatti tradizionali emiliani con opzioni di fast food sano.

## 🎯 Features

- 🎯 **Totem Interattivo**: Menu touchscreen con personalizzazione ordini
- 👨‍💼 **Dashboard Admin**: Gestione menu, ordini, statistiche
- 🍳 **Kitchen Display System (KDS)**: Visualizzazione ordini in cucina
- 📊 **Analytics**: Piatti popolari, ricavi, orari di picco
- 💳 **Pagamento Integrato**: Supporto carte e contactless
- 🔐 **Autenticazione JWT**: Sicurezza robusta
- 📱 **Responsive Design**: Desktop, tablet, mobile

## 🛠️ Stack Tecnologico

- **Frontend**: React + TypeScript + Tailwind CSS
- **Backend**: Node.js + Express + TypeScript
- **Database**: PostgreSQL
- **Real-time**: Socket.io
- **Containerization**: Docker
- **Auth**: JWT

## 📁 Struttura Progetto

```
fusionbite/
├── frontend/          # App React
├── backend/           # API Express
├── database/          # Schema PostgreSQL
├── docker/            # Configurazioni Docker
├── docs/              # Documentazione
└── README.md
```

## 🚀 Quick Start

### Prerequisiti
- Node.js 18+
- PostgreSQL 14+
- Docker (opzionale)

### Setup Locale

1. **Clone e installa dipendenze**
```bash
# Backend
cd backend
npm install
cp .env.example .env
npm run dev

# Frontend (in un altro terminale)
cd frontend
npm install
npm start
```

2. **Database**
```bash
createdb fusionbite
psql fusionbite < ../database/schema.sql
```

### Con Docker
```bash
docker-compose up -d
```

## 📖 Menu Base

### 🥗 Insalate Sane
- Insalata di Rucola e Parmigiano
- Insalata Mista Bio
- Buddha Bowl Proteico

### 🍝 Piatti Tradizionali
- Tagliatelle al Ragù
- Tortellini in Brodo
- Pappardelle ai Funghi Porcini

### 🍔 Fast Food Fusion
- Piadina Gourmet
- Burger Emiliano (ragù bolognese)
- Sandwich Romagna Style

### 🍰 Dolci
- Tiramisù Tradizionale
- Torta Barozzi (specialità modenese)
- Panna Cotta

## 🔌 API Endpoints

### Menu
- `GET /api/menu` - Lista menu
- `GET /api/menu/:id` - Dettaglio piatto
- `POST /api/menu` (admin) - Crea piatto

### Ordini
- `POST /api/orders` - Crea ordine
- `GET /api/orders/:id` - Dettaglio ordine
- `GET /api/orders` (admin) - Lista ordini
- `PUT /api/orders/:id/status` (admin/kitchen) - Aggiorna stato

### Admin
- `GET /api/admin/analytics` - Statistiche
- `GET /api/admin/kitchen` - KDS real-time

## 👥 Ruoli Utenti

- **Cliente**: Ordina dal totem
- **Admin**: Gestisce menu, ordini, statistiche
- **Kitchen**: Visualizza ordini da preparare (KDS)
- **Cashier**: Gestisce pagamenti

## 📊 Modello Dati

### Tabelle Principali
- `users` - Utenti (admin, kitchen, cashier)
- `menu_items` - Piatti disponibili
- `categories` - Categorie menu
- `orders` - Ordini
- `order_items` - Articoli per ordine
- `payments` - Pagamenti

## 🔐 Sicurezza

- JWT per autenticazione
- Password hash con bcrypt
- CORS configurato
- Rate limiting su API
- Validazione input

## 📝 TODO

- [ ] Setup database completo
- [ ] API REST completa
- [ ] Frontend totem
- [ ] Dashboard admin
- [ ] Kitchen Display System
- [ ] Sistema pagamenti
- [ ] Analytics
- [ ] Testing
- [ ] Deployment

## 👨‍💻 Autore

Vasco Manservigi

## 📄 Licenza

MIT

---

**Pronto a ordinare? 🍝🍔**
