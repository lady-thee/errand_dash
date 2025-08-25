# errand_dash
A Secure Peer-to-Peer Errand Platform API

## Introduction
**ErrandDash** is the robust and scalable backend API for a peer-to-peer platform that connects users who need errands run ("Senders") with trusted individuals in their community who can complete them ("Runners").

The core mission of this project is to develop a highly secure and trustworthy system that addresses the challenge of completing small, urgent tasks efficiently. It is engineered with a "Security First" mindset, focusing on financial integrity, data protection, and a reliable user experience.

This project is being developed as a public learning journey, emphasizing best practices in modern backend engineering over rapid development.

## Core Features (MVP)
The API is being built to support the following core functionalities:

- Secure User Authentication: A modern, passwordless authentication system built with WebAuthn/Passkeys, providing a higher level of security and a better user experience than traditional passwords. Session management is handled via JWTs.
- Distinct User Roles: A clear separation between "Sender" and "Runner" roles, each with its own set of permissions and capabilities.
- Digital Wallet System: Every user has an integrated digital wallet. Senders can securely fund their wallets via a third-party payment gateway (e.g., Paystack/Flutterwave), and Runners can initiate withdrawals.
- Payment Integration: Payments will be made via Paystack
- **Transactional Escrow Flow:** To ensure trust, all transactions are atomic and managed by an internal escrow system. When a Sender posts an errand, the total cost is securely held. Funds are only released to the Runner and the platform upon successful confirmation of completion.
- Geospatial Functionality: Enables the matching of Senders with nearby Runners based on their primary location.
- Comprehensive Errand State Management: The API manages the full lifecycle of an errand through various states, including posted, accepted, completed, confirmed, and cancelled.

## Architectural Goals & Learning Objectives
Beyond the features, this project is a deliberate exercise in mastering the following engineering principles:

- **Security First**: Implementing a secure-by-design architecture, from the passwordless authentication scheme to the encryption of sensitive user data (PII) and the integrity of financial transactions.
- **Scalability & Performance**: Leveraging the asynchronous capabilities of FastAPI and PrismaORM to build a non-blocking, high-performance API ready for future growth.
- **Data Integrity**: Designing a robust PostgreSQL database schema and using atomic transactions (ACID principles) for all financial operations to prevent data corruption and ensure reliability.
- **Third-Party Integrations**: Mastering the art of securely and reliably integrating with external services like payment gateways and geocoding APIs.
- **Cloud Deployment**: Gaining hands-on experience with deploying, configuring, and managing a production-grade application on cloud infrastructure like AWS or DigitalOcean.

### Tech Stack
Framework: FastAPI
Database: PostgreSQL
ORM: PrismaORM
Data Validation: Pydantic
Authentication: python-webauthn for Passkeys & python-jose for JWTs
Database Migrations: Alembic
Deployment Target: AWS / DigitalOcean with Docker (Final decision will be made when the project is completed)

## Getting Started
(This section will be filled out as the project progresses.)

**Prerequisites**
- Python 3.10+
- PostgreSQL Server
- An account with a payment provider (e.g., Paystack)

**Installation**
Clone the repository:
code
Bash
git clone https://github.com/ladythee/errand_dash.git
cd errand_dash


## API Documentation
Once the server is running, interactive API documentation (powered by Swagger UI) is automatically generated and available at http://localhost:8000/api/v1/docs.

Project Status
Current Phase: Design & Initial Setup

This project is under active development.
