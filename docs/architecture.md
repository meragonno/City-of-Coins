# 🏗️ Architecture Overview

## 1. System Summary

This application is a frontend-based crypto swap interface built on top of WordPress and external swap infrastructure providers.

It does not execute swaps directly on-chain. Instead, it integrates third-party swap services through embedded widgets and JavaScript-based UI controls.

## 2. High-Level Architecture

```
User
  ↓
Frontend UI (WordPress Theme)
  ↓
Provider Integration Layer (JavaScript)
  ↓
External Swap Providers
  ├── ChangeNOW 
  └── deBridge
  ↓
Blockchain Networks (handled by providers)
```

## 3. Components
## 3.1 WordPress Layer

WordPress is used only as:

Content management system (CMS)
Page routing
Theme rendering engine

It does NOT handle:

Swaps
Wallet logic
Transaction execution

## 3.2 Frontend Theme Layer

Located in:
```
themes/
```
Responsible for:

UI rendering

Swap interface layout

User interaction handling

Loading provider widgets

State transitions (loading, success, error)

## 3.3 Javascript Integration Layer

Located in:
```
themes/extendable/assets
```
This layer acts as a bridge between the UI and external providers.

## Key modules:

- changenow.js
Loads ChangeNOW widget
Handles swap interface initialization

- debridge.js
Loads and configures deBridge widget
Manages embed lifecycle

## 3.4 Swap Providers

- ChangeNOW
Instant crypto swap provider
Widget-based integration
Handles liquidity routing and execution

- deBridge
Cross-chain swap infrastructure
Handles bridging and execution
Provides embedded widget interface

## 4. Data Flow
Swap Flow (ChangeNOW / deBridge)
```
User selects asset pair
        ↓
Frontend updates UI state
        ↓
JavaScript loads provider widget
        ↓
Widget handles:
  - Wallet connection
  - Quote generation
  - Swap execution
        ↓
Transaction processed by provider
        ↓
Blockchain confirms transaction
        ↓
UI displays result (success/failure)
```

## 5. Security Model

This project follows a non-custodial architecture:

No private keys are stored
No transaction signing is handled by this application

## 6. What This System Does NOT Do

This application does NOT:

Execute smart contracts directly

Store user funds

Manage wallets internally

Run a backend matching engine

Control liquidity pools

Persist sensitive user data

## 7. Environment Assumptions

The frontend assumes:

External provider widgets are available and operational

WordPress is properly configured as CMS

JavaScript is enabled in the browser

Users connect wallets through provider widgets

## 8. Extensibility

The architecture is intentionally modular:

You can add additional providers by:
Adding javascript widgets to the frontend or integrate API endpoints through the backend to add new features/services to the platform.

## 9. Summary

This system is a frontend orchestration layer for external swap infrastructure providers. It is designed to be lightweight, modular, and provider-agnostic.
