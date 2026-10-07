# KAWACH MEET

A premium, decentralized Video Conferencing application built with privacy in mind.

## Architecture
This app runs completely via **WebRTC (Peer-to-Peer Mesh)**. The video/audio data streams directly between participants' computers without passing through any central media server. 

## How to Run Locally (For Judges/Developers)

Because this app does not rely on a centralized cloud architecture, you need to run two lightweight processes on your local machine to test it:

1. **Signaling Server (PeerJS)**: Acts as a phonebook for devices to find each other.
2. **Frontend Server**: Serves the UI.

### Step 1: Start the Signaling Server
Open a terminal and run the local PeerJS server on port 9000:
```bash
npx peer --port 9000 --key peerjs --path /myapp
```

### Step 2: Start the Web App
Open a second terminal in this directory and serve the static files:
```bash
npx serve -p 3000
```

### Step 3: Test the App
Open your browser and navigate to `http://localhost:3000`. To simulate multiple users, open another tab or a different browser on the same machine and join the same room.
