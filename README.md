# Real-Time Serverless Chat App

A fully serverless real-time chat application built on AWS using 
WebSockets. Messages are instantly broadcast to all connected 
clients without any servers to manage.

## Architecture

- **AWS API Gateway** — WebSocket connections
- **AWS Lambda** — Python backend logic
- **Amazon DynamoDB** — stores connections and messages

## Features

- Real-time messaging via WebSockets
- Multiple chat channels
- Custom nicknames
- Fully serverless — no servers to manage

## Prerequisites

- AWS Account
- AWS CLI configured
- AWS SAM CLI installed
- Python 3.x

## Deployment
```bash
git clone https://github.com/YOUR_USERNAME/serverless-websocket-chat
cd serverless-websocket-chat
sam build
sam deploy --guided
```

## Usage

Connect using wscat:
```bash
./node_modules/.bin/wscat -c wss://YOUR_ENDPOINT
```

Commands:
- `/name John` — set your nickname
- `/channel random` — switch channel
- `/help` — list commands

## Cleanup
```bash
sam delete
```

## License
MIT-0
