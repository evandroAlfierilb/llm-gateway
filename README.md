# llm-gateway

Small LLM proxy: cache, health check, latency logging

## Highlights

- Latency measured and returned per request
- POST /v1/chat with prompt/model/max_tokens
- SHA-256 keyed in-memory response cache
- Provider SDK plugs into one function

## Examples

```bash
curl localhost:8000/v1/chat \
  -H 'content-type: application/json' \
  -d '{"prompt": "hello", "model": "gpt-4o-mini"}'
```

## Install

```bash
pip install -r requirements.txt
uvicorn main:app --reload
```

## Project structure

```text
├── .github/
│   └── workflows/
│       └── ci.yml
├── docs/
│   ├── configuration.md
│   ├── faq.md
│   ├── roadmap.md
│   └── usage.md
├── examples/
│   └── quickstart.md
├── .editorconfig
├── .gitignore
├── CHANGELOG.md
├── CONTRIBUTING.md
├── LICENSE
├── main.py
└── requirements.txt
```

## Development

```bash
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
```

## 说明

个人练习项目, 谨慎用于生产环境。

## License

MIT. Do whatever you want.
