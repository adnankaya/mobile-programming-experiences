## WIRELESS DEBUGGING (macOS + Android)

### Prerequisites (Troubleshooting)
If you get "No route to host" or "Protocol fault":
*   **macOS Firewall:** Turn OFF (System Settings > Network > Firewall).
*   **macOS Local Network Privacy:** Ensure Terminal/IDE is allowed (System Settings > Privacy & Security > Local Network).
*   **Phone WiFi Setting:** Turn OFF "Use randomized MAC" or "Private WiFi Address" for this specific network.
*   **Same Subnet:** Ensure both devices are on the exact same WiFi (e.g., both on 5GHz, same SSID).

### Setup Steps
#### In your Phone
1.  **Enable Wireless Debugging in Phone:** Developer Options > Wireless debugging (Toggle ON).
#### In your Computer
2.  **Pair (First time only):**
    *   Click "Pair device with pairing code".
    *   Run: `adb pair <IP:PairingPort>` (Enter the 6-digit code).
3.  **Connect:**
    *   Look at the main Wireless debugging screen (IP & Port).
    *   Run: `adb connect <IP:ConnectPort>`.
4.  **Run:**
    *   Run: `flutter run -d <IP:ConnectPort>`.

---