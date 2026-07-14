      WAF Telemetry
         ↓
      Threat Correlation Agent
         ↓
      Finding stored
         ↓
      EventBridge custom event
         ↓
      SOAR Response Agent
         ├── Get finding
         ├── Validate status
         ├── Select playbook
         ├── Generate Bedrock summaries
         ├── Send SNS notification
         ├── Create incident record
         └── Update finding status
                  ↓
           Human analyst review
                  ↓
         Future containment workflow
