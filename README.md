# Ring

This repo contains unofficial packages to enable interaction and automation with the majority of [Ring](https://ring.com/) products

## About this fork

This fork is used by [`Recoveredd/scrypted`](https://github.com/Recoveredd/scrypted) to restore Ring device discovery for shared accounts. Ring's legacy location and device endpoints can return no locations for an account that has been invited to a location, preventing Scrypted from discovering an otherwise accessible doorbell or camera.

The fork adapts the API v3 work from [`dgreif/ring#1749`](https://github.com/dgreif/ring/pull/1749) to the Ring client revision vendored by Scrypted. It uses the v3 location, device, and event endpoints, resolves shared-device operation sets, and preserves Scrypted's streaming-specific changes. It remains necessary until equivalent support is available in the Scrypted dependency and has been verified with shared Ring accounts.

The maintained code is on `master`; the integration history remains available on `ring-shared-locations-v3`.

## Troubleshooting Issues

If you are having issues, please look for related articles in the [wiki](https://github.com/dgreif/ring/wiki) and search existing [Issues](https://github.com/dgreif/ring/issues) before opening a new Issue/Discussion

## `ring-client-api`

The [ring-client-api](./packages/ring-client-api/) is a TypeScript package designed to be used by developers to create your own apps/programs which interact with Rings api

## `homebridge-ring`

[homebridge-ring](./packages/homebridge-ring/) allows users to easily integrate Ring products into Apple HomeKit via [homebridge](https://homebridge.io/)

## Examples

See the [examples directory](./packages/examples/) for examples using the `ring-client-api`. For a full project example, see https://github.com/dgreif/ring-client-example

## Credits

I'd like to give a big thanks to a number developers who have put a lot of hard work into analyzing the
Ring api and building similar libraries which were extremely valuable in my creation of this project. Thank you all
for your hard work!

- @davglass - https://github.com/davglass/doorbot - The original node project that proved we can interact with Ring's api
- @jimhigson - https://github.com/jimhigson/ring-api - A promisified api for Ring's original line of products
- @tchellomello - https://github.com/tchellomello/python-ring-doorbell - A python api which is widely used for Ring integrations
- @mrose17 - https://github.com/homespun/homebridge-platform-ring-video-doorbell - The original Ring camera homebridge plugin
- @codahq - Thanks for all your help debugging the Ring api
- @joeyberkovitz - Great discovery work on the Ring Alarm websockets api
