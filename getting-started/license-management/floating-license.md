# Floating License

## Using Floating Licenses

### Installing a License

Activating a Floating License on a workstation is the same as loading a user key for a standard [activation.md](activation.md "mention"). The only difference is your key will have a `FL-` prefix. Just enter the key in the Activation dialog, or via `Help > Manage License`, or `Help > About > Load License`.

{% hint style="info" %}
## File Based Licenses

You can install your floating license the same way as described in [#license-file](activation.md#license-file "mention"). The only difference is that your file will be saved as `floating.lic`
{% endhint %}



### Acquiring a License

When you start Gaea, it will contact the online license server to acquire a floating license.&#x20;

If your maximum number of licenses/seats have been assigned at that moment, you will be notified. In that case, you have to wait until a license slot has been released.

### Usage and Loss of Network or License

Gaea will use \~5 minute heartbeats to keep the license alive, with an additional \~5 minute grace period to allow for network interruptions or other possibilities.

In case of network loss, or any other disruption, Gaea will release the license slot both on the client and server. However, the running instance of Gaea will simply revert to the Community Edition instead of shutting down. This is an added perk of our software that prevents excessive disruption in your work and allows you time to save your files or even try to recover the license without closing the session.

{% hint style="info" %}
In case you lose the network connection or the software crashes, then recover it, you may get a "Maximum Clients Assigned" message when trying to acquire a license. This is because your old license slot may not have been released. Just wait until the end of the current heartbeat (5 minutes or fewer) and then try again.
{% endhint %}

### Refreshing or Re-acquiring the License

The `Refresh` button in the Help > About dialog can be used to force a re-verification and re-acquisition of your license token.&#x20;

The accompanying `Release` button can be used to release the currently acquired license token and revert the running instance of Gaea to the Community Edition. A new license will be re-acquiring on the next run.

## Routing through a Proxy

If your workstation doesn't allow a direct internet connection, you can specify a proxy address through the Options dialog.

See the email you received during purchase to know which address and ports to allow through your firewall for the Floating Licenses to work with our online server, or contact Technical Support.

## Gaea Build Swarm

Gaea UI and Gaea Build Swarm are both applications that use the Gaea Engine to build terrains. Each requires a separate license to run.&#x20;

If you only have a single license for a specific workstation, you can choose the "Close and Build" option when starting a build from the Build menu. This will close Gaea and release the license so the Swarm can use it.

Moreover, this is the recommended way of building terrains in any case as the Gaea UI can often take up large portions of RAM, CPU, and GPU resources that the Build Swarm may need for an efficient run.

## Gaea2Houdini

When using Gaea2Houdini with a Floating License, ensure that "Shutdown Server" is not set to true in your node. Requesting a floating license too frequently can cause temporary security blocks for your IP.

If you intend to use Gaea2Houdini heavily, we recommend using a node-locked license for efficiency.

