# n8n Workflow — Lead Capture & Instant Notification

A simple real-world n8n workflow that receives a lead through a webhook, validates the submission, and sends a notification to a team inbox/Slack webhook.

## Workflow

`Webhook → Set/Validate Lead Data → IF valid → HTTP Request (notification) → Respond to Webhook`

## Use case

Small businesses often receive leads from websites but manually check forms and forward details. This automation standardizes the intake and immediately notifies the team.

## Tools / APIs

- n8n Webhook trigger
- n8n Set / Edit Fields
- n8n IF node
- HTTP Request node
- Any notification endpoint that accepts JSON (e.g. Slack Incoming Webhook)

## n8n import JSON

See `workflow.json` in this folder. Replace the notification URL with your own endpoint before activating it.

## Example payload

```json
{
  "name": "Aarav Sharma",
  "email": "aarav@example.com",
  "company": "Example Co",
  "message": "Interested in a demo"
}
```

## Note

The exported workflow contains no credentials or secrets. Configure credentials / webhook URLs in your own n8n instance.
