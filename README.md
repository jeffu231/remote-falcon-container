# Self host image build configuration for Remote Falcon

## Images

This compose file and action is for building images that will be hosted on ghcr.io to be pulled to a more complete docker compose file for self hosting the Remote Falcon application. This is just the minimal parts to build the images. Se Remote Falcon at the url below for more complete information about self hosting.

## Configuration

This compose file uses a few environment variables to work correctly. The hostname of the machine the control panel and viewer urls are hosted on is necessary to set it up. Remote Falcon uses a segmented domain structure where the viewer is a named subdomain on the primary host domain.

Example: If the main control panel is hosted on my-domain.org, and you have a show using the name of lightshow, the viewer host will be lightshow.my-domain.org. Environment variables are used to set those names. In addition you need to specify the number of domain parts your base host has. I.E. my-domain.org has 3 parts. This allows the remote falcon ui code to determine if it is a control panel request, or a viewer request by the number of domain parts.

Use with a .env file alongside your compose file to externalize the host settings.

Example .env file structure.

HOSTNAME=my-domain.org\
HOSTNAME_PARTS=3\
VIEWER_HOSTNAME=lightshow.my-domain.org\
CONTROL_HOSTNAME=control.my-domain.org\
CONTROL_HOSTNAME_PARTS=3\
GA_TRACKING_ID=1\
VERSION=2025.08.29\
JWT_KEY=123456\
MONGO_URI=mongodb://root:root@mongo:27017/remote-falcon?authSource=admin

See the Remote Falcon developer docs for more information.

[Remote Falcon Developer Docs](https://docs.remotefalcon.com/docs/developer-docs/welcome)

[Remote Falcon](https://remotefalcon.com)
