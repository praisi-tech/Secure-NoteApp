# SecureNotes – Encrypted Local-Only Notes App

SecureNote is a privacy-focused Android note-taking application designed for users who prioritize security, offline access, and data ownership. All notes are stored locally and protected with AES-256 encryption. The application does not use cloud storage, tracking, or external servers.

---

## Features

### Local-Only Encrypted Storage

All note content is encrypted before being inserted into the Room database. No network permissions are requested, ensuring all data stays on the device.

### AES-256 Encryption

SecureNote uses AES-256 to protect note content, attachments, and metadata. Even if the database or files are extracted, data remains unreadable without the correct key.

### Master PIN

A master PIN is required to unlock the app and is used for deriving the encryption key through a secure key-derivation function such as PBKDF2. The PIN is not stored in plaintext.

### Per-Note Password

Individual notes can be secured with an additional password. Protected notes require both the master PIN (to open the app) and the note-specific password.

### File Attachments

Notes support encrypted attachments, including:

* Images
* Voice recordings
* Documents

All attachments are encrypted and stored inside the app’s private storage.

### Category System

Notes can be organized into categories. Users can create and manage categories for easier navigation.

### Search Functionality

A fast offline search system allows users to locate notes by title or content. Decryption happens only when needed for secure on-device searching.

### Encrypted Backups

The app supports exporting and importing encrypted backup files. Backups can only be restored with the correct backup password.

### Modern UI

Built using Material Design 3 for a clean, consistent, and intuitive user experience.

### Offline and Lightweight

SecureNote does not request internet access and does not depend on external services.

---

## Security Architecture

### Encrypted Storage

Text, attachments, metadata, and categories are encrypted before being stored. Attachments are saved as encrypted files in private app storage.

### Key Derivation

Encryption keys are derived from the master PIN using PBKDF2 or an equivalent KDF.

### Per-Note Password Layer

Notes with an additional password use an extra layer of encryption.

### Encrypted Backups

Backup files are encrypted separately using a user-defined password to ensure privacy when exported.

### No Network Permissions

The app does not access or transmit data over the internet.

---

## Project Structure (Example)

```
SecureNote/
├── app/
│   ├── data/
│   ├── ui/
│   ├── util/
│   └── viewmodel/
└── README.md
```

---

## Getting Started

### Requirements

* Android Studio Hedgehog or later
* Java 17+
* Minimum SDK 24

### Build Instructions

```
git clone https://github.com/praisi-tech/Secure-NoteApp.git
cd Secure-NoteApp
```

Open the project in Android Studio, build, and run.

---

## Testing

* Unit tests for encryption/decryption
* Integrity testing for backup import/export
* PIN verification and lockout tests
* UI tests for note creation, search, and category filtering

---

## Privacy Policy

SecureNote does not collect, transmit, or store data on any external server.
All data remains local and encrypted on the user’s device.
