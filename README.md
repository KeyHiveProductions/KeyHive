# KeyHive
----

KeyHive is a powerful, open-source authentication system designed to run securely on any server while providing a centralized, cross-machine dashboard for administration. It is built to give full control over user management, roles, and sessions while maintaining strong security and flexibility.

----
### Vision

The goal of KeyHive is to provide a robust authentication platform that is self-contained, secure, and multi-server aware. Unlike traditional authentication systems, KeyHive:

Runs directly on the server you want to protect, storing all data locally.

Offers a centralized dashboard that can run on any machine, letting you manage multiple servers from one interface.

Provides super-admin capabilities above normal server admins, allowing complete control over user roles and sessions.

Ensures security with multi-layer encryption, captcha integration, and HTTPS communication.

KeyHive is open-source for transparency, but distribution is controlled to maintain the integrity of the platform.

----
### Components
####1. Server Application

- Runs on the target machine where authentication is required.

- Provides REST APIs for:

- Login, registration, and token verification

- Role assignment and user management

- Session management

- Maintains file-based storage for all users and sessions (users.json, sessions.json).

- Optional GUI displays server info (name, super-admins, status).

- Can run as a startup task or background service, ensuring continuous operation.

####2. Dashboard Application

Runs on any machine with network access to your KeyHive servers.

Provides a web-based interface (HTML/CSS/JS) for managing all servers you have access to.

Features:

Login tied to your account for secure access.

Server discovery and selection to manage multiple servers.

Full user and session management.

Role assignment, account activation/deactivation, and session revocation.

Acts as a super-admin panel, providing centralized control over multiple server instances.

Security Highlights

Multi-layer encryption: Argon2 for passwords, AES, Sodium, HMAC, and AEAD for secure storage and communication.

Captcha integration to prevent automated attacks.

HTTPS and JSON APIs ensure secure server–dashboard communication.

File-based persistence keeps all data under server owner control.

How It Works

Install the KeyHive server on your machine.

Initialize super-admin credentials for your server.

Start the server; it hosts REST APIs for user and session management.

Open the KeyHive dashboard on any machine.

Log in with your dashboard account to discover all servers you administer.

Select a server and perform administrative actions in real time.

Even if your dashboard machine is lost, you can log in from another machine and regain full control of your servers.

Why KeyHive?

Centralized control with multi-server support.

Full security with local data storage and encryption.

Flexible administration with a super-admin dashboard.

Open-source design for transparency, reliability, and trust.

Getting Started

Clone the repository and build the server using Maven.

Deploy the dashboard on any machine and connect it to your KeyHive servers via HTTPS APIs.

Configure roles, manage users, and monitor sessions with a few clicks.

License

KeyHive is open-source but restricted for redistribution. Modifications for separate distribution or rebranding are not permitted.
