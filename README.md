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

### Learnings
- system_message: Given to agents each time they are called on. Be specific about steps they should take. Be specific about the output you want.
- description: Used by the Manager of GroupChat to choose which agent should go next. it checks the last message, and is asked to pick a next agent, based on their descriptiond.
- retreive_agents: Needs both the agent and user_proxy to work. Only user_proxy agents can run functions. user_proxy agents don't have to interact with human.
- models: gpt3.5 is much faster but less reliable at orchestration. I've found that having Managers as gpt4 and then agents as 3.5 gives good results.
