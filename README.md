# Self host image build configuration for Remote Falcon

## Images

This compose file and action is for building images that will be hosted on ghcr.io to be pulled to a more complete docker compose file for self hosting the Remote Falcon application. This is just the minimal parts to build the images to avoid doing it on the deployment server that may have limited resources. See Remote Falcon at the url below for more complete information about self hosting.

## Configuration

This compose file uses a few environment variables to work correctly. These are directlky derived from the RF configuration. 

Use with a .env file alongside your compose file to externalize the host settings.

Example .env file structure.

HOSTNAME=my-domain.org\
HOSTNAME_PARTS=2\
GA_TRACKING_ID=1\
VERSION=2025.08.29\
JWT_KEY=123456\

See the Remote Falcon developer docs for more information.

[Remote Falcon Developer Docs](https://docs.remotefalcon.com/docs/developer-docs/welcome)

[Remote Falcon](https://remotefalcon.com)
