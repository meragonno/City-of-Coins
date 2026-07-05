# 🚀 City of Coins
City of Coins is an open-source frontend for a modular non-custodial crypto liquidity routing platform that integrates trusted third-party swap/defi providers through a lightweight, open-source frontend.
This repository contains the open-source frontend layer of the application.

# 🌐 Live
👉 https://www.cityofcoins.net

# 📌 Overview
This project provides a simple and modular swap interface that allows users to swap crypto assets using external liquidity providers.

It is designed as a frontend + WordPress theme integration, where WordPress is used as the content management system and the swap interface is handled through custom JavaScript.

# ⚙️ Key Features

🔄 Swap interface UI (frontend-based)

💱 Integration with ChangeNOW widget

🌉 Integration with deBridge widget

📱 Responsive design (mobile + desktop)

🎨 Custom theme-based UI layer

⚡ Lightweight JavaScript architecture

🧩 Modular provider integration system


# 🏗️ Architecture

The system is split into two parts:

1. Frontend Layer (this repository)
Handles UI and user interaction
Loads and manages swap widgets
Controls navigation and interface state

3. External Services
ChangeNOW (instant swap widget)
deBridge (cross-chain swap infrastructure)

This repository does NOT include backend infrastructure, user management, or WordPress core files.

Swap execution is handled by third party integrations. This repository only manages the frontend integration layer and user experience.


# 🧠 How It Works
User selects a swap provider (Instant Swap or DEX Mode)
Frontend loads the corresponding widget
Widget handles wallet connection and swap execution
UI updates based on widget state and events

No custom on-chain swap execution logic is implemented in this repository.


# 🚀 Getting Started (Local Setup)
1. Clone the repository
```
git clone https://github.com/meragonno/city-of-coins.git
```

3. Place theme into WordPress

Copy the theme/ folder into:
wp-content/themes/

3. Activate theme

In WordPress admin:

Appearance → Themes → Activate
4. Open swap page

Navigate to your configured swap page.

# 🔒 What’s NOT included

This repository does NOT contain:

WordPress core files
Database or user data
Backend infrastructure
API keys or secrets
Analytics or tracking systems
Production server configuration

# 📸 Screenshots

Add screenshots here:

xxx

xxx

# 📜 License

MIT License

# ⭐ Purpose

This repository exists to provide transparency into the frontend architecture and user experience layer of the swap platform, enabling developers to review, reuse, or contribute to the interface layer.

# 🤝 Disclaimer

This project is a frontend integration layer for third-party swap providers. All swap execution, liquidity routing, and blockchain interactions are handled by external services.

