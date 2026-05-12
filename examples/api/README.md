# Rivya API Examples

This directory keeps small, reviewable examples for the Rivya Public API. The maintained API docs live on the Rivya website:

- Developers: https://rivya.ai/developers
- API overview: https://rivya.ai/docs/api
- API quickstart: https://rivya.ai/docs/api-quickstart
- API authentication: https://rivya.ai/docs/api-authentication
- API models: https://rivya.ai/docs/api-models
- API model reference: https://rivya.ai/docs/api-model-reference
- OpenAPI contract: https://rivya.ai/docs/api-openapi-schema

## Example Index

### List models

Use this first when your integration needs to choose a model dynamically.

```bash
curl https://rivya.ai/api/v1/models \
  -H "Authorization: Bearer rvya_sk_your_api_key"
```

Related docs:

- https://rivya.ai/docs/api-models
- https://rivya.ai/docs/api-model-reference

### Create an image, video, or audio generation task

Use asynchronous generations for media models.

```bash
curl https://rivya.ai/api/v1/generations \
  -H "Authorization: Bearer rvya_sk_your_api_key" \
  -H "Content-Type: application/json" \
  -H "Idempotency-Key: example-request-001" \
  -d '{
    "model": "replace_with_model_id",
    "prompt": "Create a clean product visual for a launch page.",
    "params": {}
  }'
```

Related docs:

- https://rivya.ai/docs/api-generations
- https://rivya.ai/docs/api-generation-status
- https://rivya.ai/docs/api-credits

### Create a chat completion

Use Chat API for planning, analysis, content workflows, and model-supported chat tasks.

```bash
curl https://rivya.ai/api/v1/chat/completions \
  -H "Authorization: Bearer rvya_sk_your_api_key" \
  -H "Content-Type: application/json" \
  -H "Idempotency-Key: example-chat-001" \
  -d '{
    "model": "replace_with_chat_model_id",
    "message": "Draft a concise product launch checklist for a multimodal AI workflow."
  }'
```

Related docs:

- https://rivya.ai/docs/api-chat
- https://rivya.ai/docs/api-errors-and-limits

## Rules For Examples

- Do not commit real API keys.
- Do not include private customer data.
- Do not describe internal provider routing.
- Prefer links to maintained Rivya docs over copying long API reference tables.
