# Stract controller overlay

Transparent, live-input custom controller overlay. The complete application and embedded artwork are in `index.html`; no build step is required.

## Enable the browser-source URL

In this repository, open **Settings → Pages**. Under **Build and deployment**, select **Deploy from a branch**, choose **main** and **/ (root)**, and click **Save**. Wait for GitHub to report that deployment has completed and use the published URL shown there.

Expected project URL after deployment:

https://gfgggggggghhjred.github.io/Stract-controller-overlay/

The github.com repository URL is not an OBS browser-source URL.

## OBS setup

1. Add a **Browser** source.
2. Leave **Local file** unchecked and paste the deployed Pages URL.
3. Set width **1920**, height **1080**, and custom frame rate **60 FPS**.
4. Connect your controller. Use **Interact** on the source and press a controller button to allow the browser to discover it.

The background is transparent. Inputs respond immediately; this live application does not play the prerecorded demonstration or slow down real controller input.

## Inputs

Uses the browser's standard Gamepad API mapping: both analog sticks, L3/R3, D-pad, cross/circle/square/triangle, L1/R1, analog L2/R2, Create, Options, PS/Home (Cinch emblem), and touchpad click where exposed. Triggers darken continuously with pressure. Bumpers and triggers are independent. Disconnecting restores neutral artwork.

Blank face buttons retain their artwork: triangle at top, circle at right, cross at bottom, square at left. PS/Home and touchpad may be intercepted by the operating system or omitted by the input driver. Mute is not mapped. Nonstandard gamepad mappings are not guessed.

## Troubleshooting

Append `?debug=1` to the published URL to show connection and mapping status. To select a specific controller index, use `?pad=0&debug=1` (indices start at zero).

Physical controller input must be tested on the streaming computer. Browser/OBS Gamepad API availability and controller exposure depend on the installed browser engine, OS, and driver. If no controller is exposed in OBS, this page alone cannot manufacture input; an input bridge or a compatible browser capture may be needed.

## Artwork and reference

Custom Stract/Cinch artwork supplied for this project. Shoulder-control silhouettes and placement were adapted from the reference at https://github.com/philipbry/dualsense_overlay. Existing branding remains the property of its owners. No blanket license to redistribute third-party artwork is granted by this repository.
