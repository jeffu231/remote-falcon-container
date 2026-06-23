# Self host image build configuration for Remote Falcon

## Images

This compose file and action is for building images that will be hosted on ghcr.io to be pulled to a more complete docker compose file for self hosting the Remote Falcon application. This is just the minimal parts to build the images to avoid doing it on the deployment server that may have limited resources. See Remote Falcon at the url below for more complete information about self hosting.

See the Remote Falcon developer docs for more information.

[Remote Falcon Developer Docs](https://docs.remotefalcon.com/docs/developer-docs/welcome)

[Remote Falcon](https://remotefalcon.com)

## Build Action

The Github build action here creates docker images daily if the upstream RF branch has changes. Scheduled to run shortly before midnight Central time. RF Version will be the build date when a build is made.

Anyone should be able to fork this repo, configure the secrets and variables for your self hosting needs and then have your own daily images. Some knowledge of GHCR is needed along with how to create your secrets and variables.

Secrets needed:

- HOSTNAME: The hostname for your self hosted site. This is the plain host without https:// for WEB_URL in RF. Ex. example.com
- CONTROL_PANEL_SUBDOMAIN: Configure per RF guidelines. Not needed for most setups.
- GA_TRACKING_ID: Configure per RF guidelines.
- JWT_VIEWER: Configure per RF guidelines. VIEWER_JWT_KEY

Variables needed:

- HOSTNAME_PARTS: Typically 2
- TARGET_BRANCH: Typically main. This the RF branch to track for your updates.
