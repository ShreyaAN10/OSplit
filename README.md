# OSplit
A local-first and peer-to-peer expense-splitting app where users can track shared expenses, sync data offline, and manage group balances without a centralized server. The app allows individuals to add expenses and sync with others through direct or semi-direct P2P connections.

## Features

1. Offline-first: Expenses are stored locally, ensuring you can manage your data even without an internet connection.
2. Peer-to-peer sync: Sync your expenses with other users when connected over the same network or via the internet.
3. No central server: Your data is not stored on any central server — it's fully under your control.
4. CRDT-based conflict resolution: Uses CRDT (Conflict-free Replicated Data Types) to ensure that data is merged seamlessly when syncing.
5. Private and secure: All data is encrypted and signed using public-key cryptography to ensure authenticity and integrity.

## How It Works

1. Create a Group: One user creates a trip or expense group and invites others by sharing a unique code or QR.
2. Add Expenses: Users can add expenses locally on their devices — noting down who paid what, and for whom.
3. Sync with Group: Once connected, users can sync their local data with each other, either over the same network or through the internet.
4. Automatic Merging: The app automatically resolves conflicts when multiple users add or modify expenses, using CRDT-based merging logic.
5. Balances: After sync, users see the full list of expenses and their balances updated in real-time.

## Supported Platforms

Mobile: Android & iOS (built with React Native)

Web (optional): Future support for browser-based usage.

