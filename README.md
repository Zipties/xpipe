# XPipe Vault (Keep this repository private!)

This repository contains all connection information that is designated to be shared.

You can sync with this repository in all XPipe application instances the same way, every change you make in one instance will be reflected in the repository. 

## Category list

- **Connections**
  - [**Default**](categories/97458c07-75c0-4f9d-a06e-92d8cdf67c40)
- **Scripts**
- **Identities**
  - [**Synced**](categories/69aa5040-28dc-451e-b4ff-1192ce5e1e3c)

## Connection list

**All connections / Default**

- [**homestead**](stores/a7ed5760-48e2-4749-b6f5-c3326ff94a3a)
  - [**Proxmox systems**](stores/98ef287d-5335-4d5a-8d72-0f8abcbc621e)
    - [**dock-homestead**](stores/ec954d6f-e707-4980-a5bb-5713199b9b58)
      - [**Docker containers**](stores/d8fffd37-a0f0-4794-b5f4-db5e689c3d9e)
        - [**default**](stores/b4bb91b4-e783-4b7c-861b-76bd36739f16)
    - [**GhostHAS-666**](stores/f8f5ba93-ee5e-449c-b09b-a6b63491d79b)
    - [**Services**](stores/510e77ba-4763-40e7-988e-041401333799)
      - [**Dashboard**](stores/0e3f210e-42f7-42f6-a9d0-ef8440b98708)
- [**lappy**](stores/8a95f716-9f61-4074-97a5-cd36671efdf1)
  - [**Proxmox systems**](stores/88b2c11c-563d-4df9-9b2a-58ed81da43ec)
    - [**debian**](stores/cdf48555-0dbe-4404-8b95-9dd8e37866bb)
    - [**dock-lappy**](stores/93a24f62-6713-4287-9dbb-51941d783c91)
      - [**Docker containers**](stores/754d5f25-ee39-4ad5-8788-744b582c65d8)
        - [**default**](stores/ff1d81c4-c25e-4662-9677-2b3d6c21a515)
    - [**GhostHAS-1337**](stores/0cc35f69-eff4-44c2-895f-12cb604c7609)
    - [**influxdb**](stores/2607f663-ef81-48d7-b8f1-fdf7a866b9bc)
    - [**pdc**](stores/365a306c-0650-4b38-b04c-eb479768fa95)
    - [**Services**](stores/90990141-fe58-402a-b680-4e80fe8c3316)
      - [**Dashboard**](stores/344493ff-464e-4d8e-81c3-9ed470a99706)
- [**servarr**](stores/9a435a78-d258-4cfe-a427-7670ff034b33)
  - [**Proxmox systems**](stores/1ec60945-769a-4243-bcb3-17813330e4c3)
    - [**deb-tempate**](stores/03bc0265-6c0a-409f-839c-6c35c6577af8)
    - [**dock-servarr**](stores/d9261639-cf82-4cb0-9c25-9d9729a897eb)
    - [**harvest-servarr**](stores/e28b7531-4368-45db-99c6-5449a3d713ff)
    - [**homeassistant**](stores/b0ce5179-b801-46ba-a3cd-fca37e91a2cc)
    - [**plex-lxc**](stores/688d01b8-db15-4ee5-b6d8-76df0a1c5e74)
    - [**Services**](stores/40b88b5c-e414-4326-9e7c-d9f9c0cbae85)
      - [**Dashboard**](stores/27277267-3fda-4db7-b73f-fa543cf58dbf)
    - [**TrueNasScale**](stores/56655794-8149-45ef-8192-09e74913bd0c)
    - [**urbackups**](stores/d2f9a503-979d-489c-9888-bbdbb784fc6e)
    - [**window**](stores/804acc42-117c-43d4-9178-efb34db418e6)
- [**Tailscale connections**](stores/66fd26e9-8a47-49f3-9acd-2a6c6d3a6795)
  - [**ck.cpa**](stores/393a851b-6011-4c0a-9d2d-b1d6a08cfe0f)

**All identities / Synced**

- [**proxmox**](stores/76ff10ab-1731-4486-8a6e-4262596c5ccd)
- [**std**](stores/6b208234-c915-4daf-96d7-398014ecbcde)


## Secret encryption

You have the option to fetch any sensitive information like passwords from outside sources like password managers or enter them at connection time through a prompt window. In that case, XPipe doesn't have to store any secrets itself.

In case you choose to store passwords and other secrets within XPipe, all sensitive information is encrypted when it is saved using AES with either:

- A dynamically generated key file `vaultkey` (The data can then only be decrypted with that file present)
- A custom passphrase that can be set for your user in the vault settings menu (This option can only as secure as the password you choose)

By default, general connection data is not encrypted, only secrets are.
So things like hostnames and usernames are stored without encryption, which is in line with many other tools.
There is an available setting in the vault settings menu to encrypt all connection data if you want to do that.

## Cloning the repository on other systems

Nowadays, most providers require a personal access token (PAT) to authenticate from the command-line instead of traditional passwords.
You can find common (PAT) pages here:
- **GitHub**: [Personal access tokens (classic)](https://github.com/settings/tokens)
- **GitLab**: [Personal access token](https://docs.gitlab.com/ee/user/profile/personal_access_tokens.html)
- **BitBucket**: [Personal access token](https://support.atlassian.com/bitbucket-cloud/docs/access-tokens/)
- **Gitea**: `Settings -> Applications -> Manage Access Tokens section`
Set the token permission for repository to Read and Write. The rest of the token permissions can be set as Read.

Even if your git client prompts you for a password, you should enter your token unless your provider still uses passwords.

If you don't want to enter your credentials every time, you can use any git credentials manager for that.
For more information, see for example:
- https://git-scm.com/doc/credential-helpers
- https://docs.github.com/en/get-started/getting-started-with-git/caching-your-github-credentials-in-git

Some modern git clients also take care of storing credentials automatically.

## Troubleshooting

### Adding connections to the repository

By default, no connection categories are set to sync so that you have explicit control on what connections to commit.

To have your connections of a category put inside your git repository, you first need to change its sync configuration.
In your `Connections` tab under the category overview on the left side, you can open the category configuration menu either by right-clicking the category or click on the `⚙️` icon when hovering over the category, and then clicking on the `🔧` configure button.

Then, set the `Sync with git repository` value to `Yes` to sync the category and connections to your git repository.
This will add all syncable connections in that category to the git repository.
The sync settings for a category are inherited by default from its parent if not explicitly set.

### Local connections are not synced

Any connection located under the local machine can not be shared as it refers to connections and data that are only available on the local system.
