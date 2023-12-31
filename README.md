# Openai API Demo
This is a demo of the OpenAI API. It uses openai-sb as a wrapper for the API. The demo is a simple web service that generates text based on a prompt. The prompt is a text field in the web service. The generated text is displayed in the web service.

## Requirements
- Python 3.8
- OpenAI-sb API Key(https://openai-sb.com/guide/getting-started.html)

## Setup
1. Clone this repository
2. Install flit: `pip install flit`
3. Install dependencies: `flit install`

## Locally Run
1. Copy config-example.json to config.json and add your API key.
2. Start Service: 
```bash
cd openai_api_demo
uvicorn main:app --reload
```
3. Access the service at http://localhost:8000
4. API documentation is available at http://localhost:8000/docs

## Deploy to AWS
1. Install aws copilot: https://aws.github.io/copilot-cli/docs/getting-started/install/
2. Deploy to AWS: `copilot deploy -n internet-example -e test`
3. Access the service at the URL provided by copilot. It will be something like: http://internet-example-test.us-west-2.elb.amazonaws.com
4. Retrieve logs: `copilot svc logs -n internet-example -e test`