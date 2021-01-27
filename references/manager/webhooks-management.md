---
description: 'On this section, you will find information about webhooks management.'
---

# Webhooks management

The webhooks are triggered when they receive a new analysis on Horusec's database. After you have inserted this analysis, Horusec verifies if there is some configured webhook to the selected repository and sen the analysis via HTTP to the configured place.

On the webhook configuration, you have to choose:

* URL;
* Método \(for now, it is POST\); 
* Headers \(5 max\);
* Description \(optional\);
* Repository.

See the a configuration example below: 

![](../../.gitbook/assets/webhooken_us.gif)

After configuring the webhook, your API you receive a JSON with the format below: 

```go
{
  "analysisVulnerabilities": [
    {
      "analysisID": "string",
      "createdAt": "string",
      "vulnerabilities": {
        "code": "string",
        "column": "string",
        "commitAuthor": "string",
        "commitDate": "string",
        "commitEmail": "string",
        "commitHash": "string",
        "commitMessage": "string",
        "confidence": "string",
        "details": "string",
        "file": "string",
        "language": "string",
        "line": "string",
        "securityTool": "string",
        "severity": "string",
        "type": "string",
        "vulnHash": "string",
        "vulnerabilityID": "string"
      },
      "vulnerabilityID": "string"
    }
  ],
  "companyID": "string",
  "companyName": "string",
  "createdAt": "string",
  "errors": "string",
  "finishedAt": "string",
  "id": "string",
  "repositoryID": "string",
  "repositoryName": "string",
  "status": "string"
}

```

