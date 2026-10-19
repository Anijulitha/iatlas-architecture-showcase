# iatlas-architecture-showcase
 IAtlas, un SaaS de automatización contable, trabajando en procesamiento de documentos, extracción y transformación de datos, automatización de workflows y aplicación de IA a procesos empresariales.
# 🏛️ I.ATLAS - Intelligent Fiscal Document Automation SaaS

![Python](https://img.shields.io/badge/Python-3.12-blue?style=for-the-badge&logo=python)
![Streamlit](https://img.shields.io/badge/Streamlit-UI-FF4B4B?style=for-the-badge&logo=streamlit)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-DB-336791?style=for-the-badge&logo=postgresql)
![AWS S3](https://img.shields.io/badge/AWS_S3-Storage-569A31?style=for-the-badge&logo=amazon-s3)
![Railway](https://img.shields.io/badge/Railway-Deployment-0B0D0E?style=for-the-badge&logo=railway)
![Stripe](https://img.shields.io/badge/Stripe-Billing-008CDD?style=for-the-badge&logo=stripe)

> **I.ATLAS** is a B2B multi-tenant SaaS platform designed to eliminate manual data entry in accounting firms. It utilizes advanced OCR and LLM technologies to extract, audit, and export fiscal data into industry-standard ERP formats.

## 📖 Project Overview

Accounting firms spend thousands of hours manually typing invoice data into ERP systems. I.ATLAS solves this bottleneck by acting as an intelligent processing pipeline. It not only extracts data from highly unstructured PDFs but also acts as a "Mathematical Referee", mathematically auditing tax bases, VAT, and IRPF before generating import-ready files for software like Sage, Holded, Contaplus, and A3 Asesor.

## ✨ Core Features

*   **Template-Free OCR Extraction:** Parses unstructured PDFs to extract providers, dates, tax bases, and nested tax brackets using Python-based OCR (Tesseract) and LLM endpoints.
*   **Mathematical Referee Algorithm:** A strict validation layer that mathematically cross-checks totals and tax quotas. Invoices with discrepancies are flagged for manual review, ensuring 100% accounting accuracy.
*   **Direct ERP Export Pipelines:** Transforms validated data into specific structural formats, including complex fixed-length `.DAT` files for A3 Asesor and standard CSV/Excel files.
*   **Multi-Tenant Architecture:** Secure isolation of company data, managed via PostgreSQL with Alembic migrations.
*   **Integrated Billing System:** Subscription tier management (Trial, Starter, Pro, Business, Enterprise) natively integrated with Stripe API and Stripe Customer Portal.

## 🛠️ Architecture & Tech Stack

### Backend
*   **Core Logic:** Python, FastAPI, Flask
*   **Database:** PostgreSQL (with Alembic for schema migrations)
*   **Cloud Storage:** AWS S3 (Encrypted storage for sensitive PDF documents)
*   **Processing:** Background worker queues for heavy OCR/LLM document parsing.

### Frontend
*   **Framework:** Streamlit
*   **UI/UX:** Custom HTML/CSS injection to override default Streamlit components, achieving a premium corporate brand identity (Beige `#F5EDE6` & Dark Brown `#64301F`).

### Infrastructure & DevOps
*   **Containerization:** Docker
*   **Hosting:** Railway (Web services & Postgres DB)
*   **Tunnels:** Ngrok (for local webhook testing)

## 💻 Code Highlights (Showcase)

*Note: As this is a proprietary commercial product, the full source code is private. Below are architectural highlights demonstrating the technical implementation.*

1.  **[Architecture Diagram](link_to_diagram.png):** High-level overview of the PDF ingestion and processing pipeline.
2.  **`billing.py` (Snippet):** Demonstrates secure integration with Stripe Checkout and Portal sessions handling company ID metadata.
3.  **`planes_ui.py` (Snippet):** Showcases advanced Streamlit UI manipulation using injected CSS for responsive, custom-styled pricing cards.

## 🔒 Security & Compliance
*   Strict adherence to RGPD (GDPR) guidelines.
*   Documents are stored securely in AWS S3 and are only temporarily accessed in memory during processing.
*   Database-level isolation for different tenants.

---
**Developed by:** [Ana Peláez Nieto](https://github.com/tu-usuario) | Software Engineer & Creator of I.ATLAS
