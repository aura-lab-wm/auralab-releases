<p align="center">
  <img src="assets/hero.png" alt="A laptop with a terminal and a browser window, joined by a gold line through a padlocked tunnel to a GPU server with four glowing cards" width="100%">
</p>

<h1 align="center">AuraLab</h1>

<p align="center">
  <b>Sets up your Mac for the AURA Lab's AI coding tools once, then opens them for you every day.</b>
</p>

<p align="center">
  <a href="https://github.com/aura-lab-wm/auralab-releases/releases/latest"><img alt="Latest release" src="https://img.shields.io/github/v/release/aura-lab-wm/auralab-releases?label=latest&color=115740"></a>
  <img alt="macOS 12 or later" src="https://img.shields.io/badge/macOS-12%2B-0B3D2D">
  <img alt="Apple Silicon and Intel" src="https://img.shields.io/badge/Apple%20Silicon%20%2B%20Intel-universal-B9975B">
  <img alt="Signed updates" src="https://img.shields.io/badge/updates-signed-1F6B7A">
</p>

<p align="center">
  <a href="https://github.com/aura-lab-wm/auralab-releases/releases/latest"><b>Download</b></a> ·
  <a href="#install">Install</a> ·
  <a href="#the-setup-page-by-page">The setup</a> ·
  <a href="#every-day">Every day</a> ·
  <a href="#how-it-works">How it works</a> ·
  <a href="#questions">Questions</a>
</p>

AuraLab connects two AI coding clients, **Claude Code** (in a terminal) and **DeepSeek Harness** (in your browser), to
**rocco**, the AURA Lab's GPU server with four NVIDIA L40S cards. It installs what the clients need, keeps it running in
the background, and lives in your menu bar.

This repository holds only the downloads and the update feed. The source code is private.

<table>
  <tr>
    <td width="33%" align="center"><img src="assets/setup.png" alt="A laptop with four progress badges, three checked, and a green seal" width="100%"></td>
    <td width="33%" align="center"><img src="assets/daily.png" alt="A laptop menu bar with a small gold icon and a menu offering a terminal and a browser" width="100%"></td>
    <td width="33%" align="center"><img src="assets/signed.png" alt="A parcel sealed with green wax stamped with a key, next to a shield" width="100%"></td>
  </tr>
  <tr>
    <td valign="top"><b>Set up once.</b> Four pages: pick your client, type what your instructor gave you, wait for ten steps, done.</td>
    <td valign="top"><b>Open it every day.</b> AuraLab sits in the menu bar, shows whether everything is up, and opens your client.</td>
    <td valign="top"><b>Signed updates.</b> New versions arrive from this repository. AuraLab installs only an update whose signature matches.</td>
  </tr>
</table>

## Install

macOS 12 or later, Apple Silicon or Intel.

1. Download the `.dmg` from the [latest release](https://github.com/aura-lab-wm/auralab-releases/releases/latest).
2. Open it and drag **AuraLab v1** to **Applications**.
3. Open **AuraLab v1** from Applications. This build is not notarized by Apple yet, so macOS blocks the first open:
   go to **System Settings → Privacy & Security**, find the line about AuraLab v1 and click **Open Anyway**. You do this once.
4. Follow the four pages of the setup (below). Your instructor gives you your username and the server address.

> [!NOTE]
> Run AuraLab from **Applications**. Started from the disk image or from Downloads, it asks you to move it first: the
> login item and the Dock point to where it lives.

## The setup, page by page

<table>
  <tr>
    <td width="50%"><img src="assets/screens/1-clients.png" alt="Setup page 1: choose Claude Code, DeepSeek Harness or both"></td>
    <td width="50%"><img src="assets/screens/2-account.png" alt="Setup page 2: username, server address and your SSH public key with a Copy button"></td>
  </tr>
  <tr>
    <td valign="top"><b>1 · Clients.</b> Pick Claude Code, DeepSeek Harness (DSH), or both. With both, AuraLab asks each day which one to open.</td>
    <td valign="top"><b>2 · Account.</b> Type your username on rocco and the server address. Click <b>Copy</b> next to your SSH public key and send the key to your instructor.</td>
  </tr>
  <tr>
    <td width="50%"><img src="assets/screens/3-installing.png" alt="Setup page 3: ten install steps with a progress bar and an elapsed clock"></td>
    <td width="50%"><img src="assets/screens/4-done.png" alt="Setup page 4: this Mac is ready, with the next steps"></td>
  </tr>
  <tr>
    <td valign="top"><b>3 · Install.</b> Ten steps run in order; the current one is highlighted. Keep the window open until the last one finishes.</td>
    <td valign="top"><b>4 · Done.</b> The next steps, and a button that opens your client. AuraLab now lives in your menu bar.</td>
  </tr>
</table>

Keyboard: **Enter** takes the page's main action (Continue, Install, Retry), **Esc** goes back from the Account page.

## Every day

<table>
  <tr>
    <td width="42%" align="center"><img src="assets/screens/6-menubar.png" alt="The AuraLab menu: gateway, shim, tunnel and DSH up; the model loaded on rocco; four GPU cards showing who holds each one; actions; the version and Check now" width="320"></td>
    <td width="58%" valign="top">
      <p>Click the AuraLab icon in the menu bar to see:</p>
      <ul>
        <li>whether the <b>gateway</b>, the <b>shim</b>, the <b>tunnel</b> to rocco and <b>DSH</b> are up, with a <b>Restart</b> button on any that is down;</li>
        <li>the <b>model</b> loaded on rocco, or why none is (no GPU free, or it loads on your first request);</li>
        <li>rocco's four <b>GPUs</b>: how much memory each one uses and who holds it, with a standing grant or a lease, or <b>free</b>;</li>
        <li><b>Open Claude Code</b>, <b>Open DSH</b>, <b>Switch model…</b>, <b>Copy SSH key</b>, <b>Restart services</b>, <b>Copy diagnostics</b>, and <b>Install update</b> when one is available;</li>
        <li>your AuraLab version, when it last looked for updates, and <b>Check now</b>.</li>
      </ul>
      <p>With both clients installed, AuraLab asks which one to open and remembers your answer:</p>
      <img src="assets/screens/5-chooser.png" alt="Which client to open today: Claude Code or DeepSeek Harness, with Remember my choice" width="100%">
    </td>
  </tr>
</table>

### Switch the model

<table>
  <tr>
    <td width="42%" align="center"><img src="assets/screens/7-switch.png" alt="Switch model: the list of rocco's models, and rocco's answer that the loaded model is in use by someone else until 14:52 UTC, with Tell me when a GPU is free" width="320"></td>
    <td width="58%" valign="top">
      <p><b>Switch model…</b> lists the models rocco can load. Click one to ask rocco to load it. The lab's rules
      decide, the same as <code>rocco-switch</code> on the server:</p>
      <ul>
        <li>a model someone else used in the last 10 minutes stays loaded;</li>
        <li>the model needs enough free GPUs;</li>
        <li>each account can switch 6 times an hour.</li>
      </ul>
      <p>When rocco says no, the menu shows its reason, word for word. If a GPU is all you are waiting for, click
      <b>Tell me when a GPU is free</b>: AuraLab checks every minute, for up to 4 hours, and sends one notification.</p>
    </td>
  </tr>
</table>

The same from Terminal:

```sh
auralab status                 # gateway, shim, tunnel and DSH
auralab gpus                   # the model on rocco and who holds each GPU
auralab models                 # the models rocco can load
auralab switch rocco-glm       # ask rocco to load one (it says why if it cannot)
auralab key                    # print your SSH public key again
auralab diagnostics            # a report for your instructor (keys and your home folder removed)
auralab launch --client dsh    # open DeepSeek Harness
```

## How it works

<p align="center">
  <img src="assets/how-it-works.svg" alt="On your Mac, Claude Code reaches rocco through a local gateway (127.0.0.1:4000), a switch shim (127.0.0.1:4010) and an SSH tunnel (127.0.0.1:8000); DeepSeek Harness goes straight to the shim. Claude models go through your own Claude account. AuraLab in the menu bar keeps the services running and installs signed updates from this repository." width="100%">
</p>

Claude Code sends requests for rocco's models to a **gateway** on your Mac (LiteLLM, `127.0.0.1:4000`), which passes
them to the **switch shim** (`127.0.0.1:4010`); DeepSeek Harness talks to the shim directly. The shim sends them through
an **SSH tunnel** to rocco, which signs in with your own key and account. Claude Code's Claude models use your own Claude
account. All three services start with your Mac.

<details>
<summary><b>The ten setup steps</b></summary>

| # | Step | What it sets up |
|---|------|-----------------|
| 1 | Check this Mac | Checks the Mac before anything is changed. |
| 2 | Python toolchain (uv) | `uv` in `~/.local/bin`. |
| 3 | Gateway backend (LiteLLM + switch-shim) | The gateway and the shim, in `~/.rocco/gateway`. |
| 4 | Gateway key | A key for your local gateway. |
| 5 | SSH access to rocco | Your SSH key (`~/.ssh/id_ed25519`) and a `Host` block in `~/.ssh/config`. |
| 6 | Background services | The gateway, the shim and the tunnel, started with your Mac. |
| 7 | Shell setup (`~/.zshrc`) | A marked block: `~/.local/bin` on your `PATH`, the `claude` wrapper that points Claude Code at the gateway, and the variable DSH's rocco route reads. |
| 8 | Claude Code | Installed if you picked it. |
| 9 | DeepSeek Harness | Installed with the rocco route and dsh-model-hub, if you picked it. |
| 10 | Check | Checks that the gateway and the shim answer. |

</details>

## Updates

AuraLab checks this repository's latest release when you log in and every 12 hours, and **Check now** at the bottom of
the menu checks at once. When a new version is out, a notification says so, once per version: click it, or the
AuraLab icon, to open the menu. Every update is signed, and AuraLab refuses one whose signature does not match.

Click **Install update**: the menu shows the download and the install as they happen. AuraLab restarts and brings its background services (the gateway and the switch shim) up to
the new version on its own, then shows a notification. Your SSH key, your logins and your settings stay as they are. If
that step fails, the menu bar shows **Finish update**: click it to run the step again.

## Questions

<details>
<summary><b>macOS says AuraLab cannot be opened</b></summary>

This build is not notarized yet. Go to **System Settings → Privacy & Security**, find the line about AuraLab v1 and click
**Open Anyway**. You do this once.
</details>

<details>
<summary><b>The setup finished, but the tunnel is not up</b></summary>

The tunnel connects once your instructor has added your SSH key to your account on rocco. Send the key if you have not
(menu bar → **Copy SSH key**, or `auralab key`), then check the menu bar or `auralab status`.
</details>

<details>
<summary><b>The setup stopped at a step</b></summary>

The page names the step and shows the error. Click **Copy details** and send the text to your instructor, or click
**Retry**. The logs are in `~/.config/rocco/logs`. If step 1 stopped, nothing was changed on your Mac.
</details>

<details>
<summary><b>Something does not work</b></summary>

Menu bar → **Copy diagnostics**, and paste the text in a message to your instructor. It holds AuraLab's version, the
checks, rocco's GPUs and the end of each log, with keys, tokens and your home folder removed. AuraLab sends it nowhere
itself. `auralab diagnostics` prints the same.
</details>

<details>
<summary><b>I need my SSH key again</b></summary>

Menu bar → **Copy SSH key**, or run `auralab key`.
</details>

## Uninstall

In Terminal:

```sh
"/Applications/AuraLab v1.app/Contents/MacOS/auralab-app" uninstall
```

then drag AuraLab v1 from Applications to the Trash. The uninstall stops and removes the background services and the
gateway. It leaves your SSH key and the `Host` block in `~/.ssh/config`, Claude Code, DeepSeek Harness and your logins.
Open a new terminal afterwards so the shell forgets the `claude` wrapper.

---

<p align="center">
  <sub><b>AURA Lab</b> · AI for Understandable and Responsible Automation in Software Engineering · William &amp; Mary</sub><br>
  <sub>Illustrations made with Gemini 4 Argon. Screenshots are of the app itself, with example data.</sub>
</p>
