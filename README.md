# Autogen Notebooks
Python notebooks for playing around with autogen powered AI Agents.

### Add API ENDPOINTS:
Create a file in same folder called `OAI_CONFIG_LIST.json`, with contents similar to:

```json
[
  {
    "model": "gpt-4-1106-preview",
    "api_key": ""
  },
  {
    "model": "gpt-3.5-turbo",
    "api_key": ""
  },
  {
    "model": "local-model",
    "api_key": "NULL",
    "base_url": "http://localhost:1234/v1",
    "api_type": "open_ai"
  }
]
```
_Note: The `local-model` is optional._

### Notebook 101
1. Open the notebook file `ipynb` in VS Code
2. VS Code will suggest necessary extensions, install them.
3. Use "Run all" to set everything up
4. Tell it your task.
5. When re-running, it is recommended to delete `.cache/` folder and change `CACHE_SEED` constant first.
