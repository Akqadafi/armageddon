Medium and High

    {
      "source": ["seir.waf.correlation"],
      "detail-type": ["WAF Threat Finding Created"],
      "detail": {
        "severity": ["MEDIUM", "HIGH"]
      }
    }

  Target: soar-response-agent

  Critical

      {
      "source": ["seir.waf.correlation"],
      "detail-type": ["WAF Threat Finding Created"],
      "detail": {
        "severity": ["CRITICAL"]
      }
    }

  Targets:

      soar-response-agent
      critical-alert SNS topic
