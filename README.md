# SecureNote – Encrypted Local-Only Notes App

SecureNote is a privacy-focused Android note-taking application. All notes are stored locally on the device and protected with AES-256 encryption and a master PIN. No cloud storage, no tracking, and no external servers.

---

## Features

### Local Storage Only

Notes are stored in an encrypted Room database on the user’s device. No cloud sync or data transmission.

### AES-256 Encryption

All note content is encrypted before being written to the database to ensure confidentiality even if the file is accessed.

### Master PIN

A master PIN is used to unlock the app and derive the encryption key. The PIN is never stored in plaintext.

### Encrypted Backups

Users can export an encrypted backup file. Without the backup password, the file cannot be decrypted or imported.

### Modern UI

Built using Material Design 3 components with a clean and minimal interface.

### Offline and Lightweight

The app requires no internet access and does not depend on any external services.

---

## Security Architecture

### Encrypted Storage

All note text is encrypted before insertion into the Room database.

### Key Derivation

Encryption keys are derived from the master PIN using a secure key-derivation function (such as PBKDF2).

### Encrypted Backups

Backup files are separately encrypted to remain private even when stored externally.

### No Network Permissions

The application does not request internet access, reducing the attack surface and preventing data transmission.

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

* Android Studio (Hedgehog or later)
* Java 17+
* Minimum SDK 24

### Build Instructions

```
git clone https://github.com/yourusername/SecureNote.git
cd SecureNote
```

Open the project in Android Studio, build, and run.

---

## Roadmap

* Dark mode
* Master PIN unlock
* Search functionality
* Folder organization
* Optional plaintext export
* Integration with Android Keystore

---

## Testing

* Encryption and decryption tests
* Backup file integrity tests
* PIN validation and lockout tests
* UI tests

---

## Privacy Policy

SecureNote does not collect data, does not transmit any information, and does not store anything on external servers. All data remains encrypted on the device.

---


