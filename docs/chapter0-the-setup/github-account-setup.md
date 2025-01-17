---
sidebar_position: 4
---

# 0.4 Github Account Setup

[Youtube 📺](https://www.youtube.com/watch?v=Am9417a87zU&t=600s)

We'll be exclusively using Github for CI (Continuous Integration) and Github Actions (Continuous Delivery) throughout this course. Hence, its critical to set things up as required to run this training smoothly.

## 🔑 SSH Key

In this section we'll setup the Github repository and configure Github access which will be used throughout the course.

- Open the terminal by clicking on hamburger menu at extreme top-left of , Terminal , New Terminal.
- Configure and copy the SSH Key using the following commands

```bash
cd ~
ssh-keygen
cat ~/.ssh/id_rsa.pub
```

![](img/1A_7.png)

- Open <a href="https://github.com/settings/keys">https://github.com/settings/keys</a> where you signed-in recently.
- Copy the public ssh key in the respective section and click on `Add SSH Key`.

![](img/1A_8.png)

## ⚙️ SSH Config

Its a good idea at this point to also add an ssh config so that we can easily work with github.com through ssh.

1. Create the config file
   
```bash
cd ~
touch ~/.ssh/config
```

2. Open the Config file using the Open Folder command as shown below

![](img/open_config.png)

3. Add the following lines to your config file and save it.

```config
Host github.com
    HostName github.com
    User git
    IdentityFile ~/.ssh/id_rsa
```

4. Test connectivity to Github

```bash
chmod 600 ~/.ssh/id_rsa
ssh github.com
```

## 🌟 Create a Github Repository

- Create a new repository by visiting the link <a href="https://github.com/new" target="_blank">https://github.com/new</a> and name it as `playground`
- Ensure visibility is private.

:::danger Repository Name

For progressing with this course ensure that the name of your repository is `playground` as lot of commands ahead will be based on this name.

:::

![](img/1A_9.png)

That's all your Github setup is good to go 🎉

:::note End of Chapter 0

That completes the Chapter 0, before you move on to Chapter 1 ensure that

- Your [AWS Account](/docs/chapter0-the-setup/aws-setup.md) has been setup
- Your [Domain](/docs/chapter0-the-setup/domain-setup.md) has been setup
- Your [Cloud Desktop](/docs/chapter0-the-setup/cloud-desktop-setup.md) has been setup
- Your [Github Account](/docs/chapter0-the-setup/github-account-setup.md) has been setup.
:::
