
# API Reference

Use the following endpoints to interact with the Apitex Cloud System.

## Authentication
All requests must include an `Apitex-Key` in the header.

```bash
curl -X GET https://api.apitex.cloud/v1/status \
     -H "Apitex-Key: YOUR_PIXEL_KEY"
```

## Endpoints

### `GET /system/health`
Retrieve the health status of the cloud's neural system.

**Response:**
```json
{
  "status": "OPERATIONAL",
  "neural_load": "12%",
  "active_agents": ["APEX", "KORE"],
  "fabric_integrity": 0.99
}
```

### `POST /orchestrate/deploy`
Deploy a new service into the fabric.

**Payload:**
```json
{
  "service_name": "Nebula-App",
  "scaling": "auto",
  "priority": "high"
}
```
