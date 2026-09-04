# tools-macos

Assorted helper scripts for macOS. They automate small development chores — pointing the system at a local debugging proxy and trusting its certificate in iOS simulators — that are tedious to click through by hand.

## Usage

Route the Wi-Fi service's HTTP and HTTPS traffic through a proxy on `localhost` at the given port:

```sh
proxy/enable_proxy 8080
```

Turn the proxy off again:

```sh
proxy/disable_proxy
```

Install a root CA certificate into the keychain of every booted iOS simulator, so the simulator trusts an intercepting proxy (requires Xcode and `jq`):

```sh
proxy/install_ca_cert_on_booted_sim ~/certs/proxy-ca.pem
```
