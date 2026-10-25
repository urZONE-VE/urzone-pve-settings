# urZONE PVE Settings

**By Osiris Simmons (Osiris83)**

If you run Proxmox VE behind WordPress with urZONE PVE Core, you need somewhere to tell WordPress how to reach your server. That is the job of **urZONE PVE Settings**. It adds a "urZONE PVE" menu to your WordPress admin so you can connect Proxmox, set defaults and limits, and test the connection without hand-editing configuration files.

Settings comes in two editions: a free one that covers everything you need to get connected, and a Pro edition that adds the web shell and license tabs. Here is what each includes and who each one is for.

## What both editions do

Both editions share the same settings page, the same look, and the same safe way of saving. When you press Save, the plugin writes your values into `wp-config.php` for you, keeps a backup of the previous file, and shows you the exact lines to paste in yourself if the file is not writable.

1. **Connection.** Choose between your own Proxmox server (API URL, user, token ID and token secret) or a hosted connection. Save and test straight from the page to confirm WordPress can talk to Proxmox.
2. **Defaults & limits.** Set the default node, storage, network bridge, container template storage and ISO storage. Choose whether to verify SSL certificates, how often the dashboard refreshes, the maximum instances for users without a plan, and the ceilings for CPU cores, memory and disk per instance.

## What Pro adds

3. **Web shell.** Turns on the Shell button for containers and VMs. You enter the address of your shell bridge and the secret it shares with WordPress, and the secret is kept in `wp-config.php` and never shown again. Pro also includes a step-by-step install guide for the bridge, right inside the settings page.
4. **License.** Enter and check your Core license key from the admin area. The plugin re-checks it once a day and shows a clear status chip, so you always know whether your license is active.

Pro also gives you live status chips in the page header showing whether the web shell and your license are active at a glance.

## Side-by-side comparison

| Feature | Settings (Free) | Settings Pro |
|---|:---:|:---:|
| Connect to your own Proxmox server | Yes | Yes |
| Hosted connection option | Yes | Yes |
| Save and test connection | Yes | Yes |
| Defaults: node, storage, bridge, ISO and template storage | Yes | Yes |
| Size limits: cores, memory, disk | Yes | Yes |
| Auto-write to `wp-config.php` with backup | Yes | Yes |
| Manual copy-and-paste fallback | Yes | Yes |
| Tab 3: Web shell settings | No | Yes |
| Built-in web shell install guide | No | Yes |
| Tab 4: Core license key entry and checks | No | Yes |
| Web shell and license status chips | No | Yes |

## Which one should you choose?

**Choose Free** if you want to get a Proxmox panel running on WordPress quickly. You get a clean connection screen, sensible defaults and limits, and a connection test, which is everything most sites need on day one.

**Choose Pro** if you want your customers to open a terminal in their containers and VMs, or you want to manage your Core license from the same screen. The web shell tab walks you through the setup, so you are not piecing it together from separate documentation.

## Good to know

Settings Pro is a convenience layer. It does not change how urZONE PVE Core behaves; it gives you a guided screen for options that otherwise live in `wp-config.php`. Install only one edition at a time. They share the same menu, so activating both is not useful.

## Get started

Ready to get started? Download the edition that fits your setup from [urzone.org](https://urzone.org) and connect your first Proxmox server in a few minutes.
