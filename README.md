# Hyper-V Launcher

**Your virtual machines. Ready when you are.**

Hyper-V Launcher makes your local Hyper-V virtual machines easier to access. Create desktop and Start Menu shortcuts, launch a VM from the system tray, and choose what happens when its connection window closes.

[Download](https://github.com/andrezammit/hypervlauncher-site/releases/latest/download/HyperVLauncher.Setup.exe) · [Visit the website](https://hypervlauncher.andrezammit.com/) · [Read the guide](https://hypervlauncher.andrezammit.com/guide.html)

Windows x64 · Hyper-V required

![Hyper-V Launcher showing shortcuts for Windows and Ubuntu virtual machines](Images/MainWindow.png)

## Shortcuts where you need them

Give each VM a recognizable shortcut on your desktop, in the Start Menu, or both. Launch it directly, or use the launcher's Shortcuts page to open and manage your configured machines.

![Virtual Machines page with the Create Shortcut action](Images/VirtualMachines.png)

## Launch from the system tray

Your configured VM shortcuts are available from the Hyper-V Launcher tray menu. Open a machine without first opening the management window, and enable **Start on Windows login** to keep the tray application available after you sign in.

![Hyper-V Launcher system tray menu](Images/TrayApp.png)

## Choose what happens next

Each shortcut can leave the VM in its current state, save its state using **Pause the Virtual Machine**, or request a shutdown when its connection window closes.

Choose the action when creating a shortcut or edit an existing shortcut later. See the [guide to close actions](https://hypervlauncher.andrezammit.com/guide.html#close-actions) for behavior and shutdown considerations.

![Shortcut settings with desktop and Start Menu options and a close action](Images/CreateShortcut.png)

## Start a VM from a remote connection

Enable **Start shortcut from remote connection** on a shortcut to start its VM when a client connects to a chosen port on the Hyper-V host. Hyper-V Launcher forwards the connection to the configured destination port inside the guest.

For Remote Desktop, enable it in the guest, choose an unused host port such as **3390**, and set the remote port to the guest's listening port, usually **3389**. Keep **Hyper-V Launcher Service** running, then connect your Remote Desktop client to the host, for example `my-hyperv-pc:3390`, using the guest's credentials. The guest must be reachable from the host; use a trusted network or VPN for remote access.

The shortcut's close action can also run after remote connections disconnect. See the [remote connection guide](https://hypervlauncher.andrezammit.com/guide.html#remote-connections) for setup, connection readiness, and close-action behavior.

## Keep your shortcuts in sync

In **Settings**, enable automatic shortcut creation for newly detected VMs, or choose to be prompted first. You can also enable cleanup to remove associated shortcuts when a VM is deleted. Settings are saved as you change the checkboxes, and automatic creation and cleanup require **Hyper-V Launcher Service** to be running. For existing VMs, create shortcuts from the **Virtual Machines** page.

## Get started

1. Make sure Hyper-V is enabled and your VM is available locally in Hyper-V Manager.
2. [Download the setup](https://github.com/andrezammit/hypervlauncher-site/releases/latest/download/HyperVLauncher.Setup.exe) and install Hyper-V Launcher.
3. Open **Hyper-V Launcher Console** from the Start Menu.
4. Select a VM on the **Virtual Machines** page and choose **Create Shortcut**.

The [illustrated guide](https://hypervlauncher.andrezammit.com/guide.html) covers requirements, shortcut creation, close actions, remote connections, automatic shortcut management, and troubleshooting.

[MSI installer](https://github.com/andrezammit/hypervlauncher-site/releases/latest/download/HyperVLauncher.Setup.Installer.msi) · [All releases and release notes](https://github.com/andrezammit/hypervlauncher-site/releases)

Created by [André Zammit](https://andrezammit.com).
