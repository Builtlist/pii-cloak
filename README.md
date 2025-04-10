# pii-cloak
Middleware that tokenises sensitive data before prompting to an LLM. 

┌──────────────┐       ┌─────────────────────────┐       ┌──────────────┐
│  Data Source │─────▶│ Tokenization Middleware │─────▶│     LLM       │
│ (DB/API/File)│       │  (This Solution)        │       │ (OpenAI etc.)│
└──────────────┘       └─────────────────────────┘       └──────────────┘
                              ▲       │
                              │       ▼
                      ┌────────────────────┐
                      │ Policy & Rules API │
                      └────────────────────┘
