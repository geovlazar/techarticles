---
author: "Geo V L"
date: 2023-06-19
linktitle: Remote Development using SSH
nomenu:
  main:
    parent: tutorials
next: /tutorials/github-pages-blog
prev: /tutorials/automated-deployments
title: Remote Development using SSH
tags : [
    "infrastructure",
    "development",
]
weight: 10
image: img/writing.jpg
authorAvatar: hugo-logo.png
---

If you need to edit and debug on a remote machine with VS Code, Install Visual Studio Code [Remote - SSH](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-ssh) extension which helps connect to a remote running SSH server and take full advantage of VS Code's feature set.

Prerequisites:

To get started, you need to have done the following steps:

1. Install an [OpenSSH compatible SSH client](https://code.visualstudio.com/docs/remote/troubleshooting#_installing-a-supported-ssh-client) (PuTTY is not supported).
2. Details of remote host machine with pre installed home-creators, SSH username and private Key.

Connect to a remote host:-

To connect to a remote host for the first time, follow these steps:

1. Place your SSH key provided inside **.ssh** directory in your home folder or at any secure location in your Windows/Linux/Mac machine. eg:- `C:\Users\username\.ssh\MachineName-username.key`
2. Make sure proper [file permissions](https://code.visualstudio.com/docs/remote/troubleshooting#_fixing-ssh-file-permission-errors) are set.
3. Verify you can connect to our SSH host by running the following command from a terminal / PowerShell window as below,
`ssh -i ~/.ssh/MachineName-username.key username@server -p 522`
4. In VS Code, select **Remote-SSH: Connect to Host...** from the Command Palette (`F1, Ctrl+Shift+P`) and use the same command as in step 3.
5. If VS Code cannot automatically detect the type of server you are connecting to, you will be asked to select the type manually, choose **Linux**.
6. After a moment, VS Code will connect to the SSH server and set itself up.
7. You can then open any folder or workspace on the remote machine using File > Open... or File > Open Workspace... just as you would locally!

#### References

[docs/remote/ssh](https://code.visualstudio.com/docs/remote/ssh)
[docs/remote/ssh-tutorial](https://code.visualstudio.com/docs/remote/ssh-tutorial)