# Inventory Management Desktop System

A professional, multi-user inventory management software built as a
native desktop application with a cloud-connected backend.

This project demonstrates enterprise-grade inventory workflows including
purchase orders, goods receipt, stock adjustments, real-time sync and
automation using n8n.

------------------------------------------------------------------------

## Features

-   Native Desktop Application (PySide6)
-   Multi-user realtime inventory synchronization
-   Barcode scanning with webcam
-   Purchase Orders, GRN, Transfers, Adjustments
-   Offline mode with auto-sync
-   Role-based access control
-   Audit logs & tamper-proof stock ledger
-   Automated alerts using n8n
-   PDF & Excel reports
-   Dockerized backend

------------------------------------------------------------------------

## Architecture

    Desktop App (PySide6)
            |
            v
    FastAPI Backend  ---> PostgreSQL Database
            |
            +--> n8n Automation Engine

------------------------------------------------------------------------

## Technology Stack

  Layer        Technology
  ------------ -------------------------
  UI           PySide6 (Qt for Python)
  Framework    FastAPI
  Database     PostgreSQL
  ORM          SQLAlchemy
  Auth         JWT + OAuth2
  Automation   n8n
  Packaging    PyInstaller
  Reports      Pandas + ReportLab
  Barcode      PyZbar + OpenCV
  Deployment   Docker + Compose

------------------------------------------------------------------------

## Installation

### Backend

    cd inventory-desktop
    docker-compose up -d

### Desktop Client

    cd client
    pip install -r requirements.txt
    python main.py

------------------------------------------------------------------------

## Packaging

    pyinstaller --noconsole --onefile main.py

------------------------------------------------------------------------

## Automations

Import `automations/n8n-flows.json` into your n8n instance to enable:

-   Low stock email alerts
-   Near expiry notifications
-   Overdue purchase order reminders
-   Daily stock summary reports

------------------------------------------------------------------------
