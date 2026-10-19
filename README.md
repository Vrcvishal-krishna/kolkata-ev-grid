# Greater Kolkata & Howrah Metropolitan EV Charging Telemetry Command Center

Live operational command center and high-precision telemetry engine for the twin-city Kolkata & Howrah metropolitan area across the Hooghly River corridor.

### Network Coverage
- **Metropolitan Grid:** 151 deduplicated public charging hubs
- **Hardware Capacity:** 650 physical guns | 26,372.3 kW installed grid load
- **CPO Integration:**
  - ChargeZone: 269 sockets
  - Jio-bp pulse (GOBP): 158 sockets
  - Statiq Network: 122 sockets
  - Tata Power EZ Charge: 69 sockets
  - goEgo Network: 20 sockets
  - BPCL: 12 sockets

### Architecture & Standby Policy
- **Zero Synthetic Data:** 100% genuine hardware telemetry directly queried from CPO cloud APIs and OCPP gateways.
- **Standby Baseline:** Default state is locked at `{"running": false}` (0 active charging, real Available/Faulted baseline). Polling daemon activates strictly when triggered via `[▶ START LIVE TELEMETRY]`.
- **Zero Cross-City Contamination:** Isolated registry bounded strictly between latitudes 22.35–22.85 N and longitudes 88.15–88.60 E.

### Deployment
Configured for automated zero-dependency deployment on Render using standard Python HTTP server and SQLite:
```bash
python app.py
```
