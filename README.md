# Snippets Text Two Factor Authentication
This snippet will show you how to implement basic two factor authentication via an text message.
## About Text Two Factor Authentication
Create an authenication request from your application, and present a challenge via text message that can be verified by a web call.
## Getting Started
You will need a machine with Python installed, the SignalWire SDK, a provisioned SignalWire phone number, and optionaly Docker if you decide to run it in a container.

For this demo we will be using Python, but more languages may become available.

- [x] Python
- [x] SignalWire SDK
- [x] SignalWire Phone Number
- [x] Docker (Optional)
----
## Running Text Two Factor Authentication - How It Works
## Methods and Endpoints

```
Endpoint: /request-auth
Methods: GET OR POST
Request a text challenge session, GET or POST 'number' to create a challenge session.
```

```
Endpoint: /validate-auth
Methods: GET OR POST
Validate a text challenge session, GET or POST 'number' and 'auth_code' to vaidate.
Will return 200 (OK) or 403 (Forbidden)
```

## Setup Your Enviroment File

1. Copy from example.env and fill in your values
2. Save new file callled .env

Your file should look something like this
```
## This is the full name of your SignalWire Space. e.g.: example.signalwire.com
SIGNALWIRE_SPACE=
# Your Project ID - you can find it on the `API` page in your Dashboard.
SIGNALWIRE_PROJECT=
# Your API token - you can generate one on the `API` page in your Dashboard
SIGNALWIRE_TOKEN=
# The phone number you'll be using for this Snippets. Must include the `+1` , e$
SIGNALWIRE_NUMBER=

```

## Build and Run on Docker
Lets get started!
1. Use our pre-built image from Docker Hub 
```
For Python:
docker pull signalwire/snippets-text-two-factor-auth:python
```
(or build your own image)

1. Build your image
```
docker build -t snippets-text-two-factor-auth .
```
2. Run your image
```
docker run --publish 5000:5000 --env-file .env snippets-text-two-factor-auth
```
3. The application will run on port 5000

## Build and Run Natively
For Python
```
1. Replace environment variables
2. From command line run, python3 app.py
```

----
# More Documentation
You can find more documentation on LaML, Relay, and all Signalwire APIs at:
- [SignalWire Python SDK](https://github.com/signalwire/signalwire-python)
- [SignalWire API Docs](https://docs.signalwire.com)
- [SignalWire Github](https://gituhb.com/signalwire)
- [Docker - Getting Started](https://docs.docker.com/get-started/)
- [Python - Gettings Started](https://docs.python.org/3/using/index.html)

# Support
If you have any issues or want to engage further about this Signal, please [open an issue on this repo](../../issues) or join our fantastic [Slack community](https://signalwire.community) and chat with others in the SignalWire community!

If you need assistance or support with your SignalWire services please file a support ticket from your Dashboard. 

