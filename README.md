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

- [**homestead**](stores/cd7f928c-5800-4312-956f-032284930316)
  - [**Proxmox systems**](stores/1b8fa294-3e1f-4271-a751-4faed7ed8c67)
    - [**dock-homestead**](stores/c5680ad9-cae0-4b2e-9fca-49cdc9328b9c)
    - [**homeassistant**](stores/74815f7e-16d5-4e9b-8583-38ecb2f32598)
    - [**MacOS Server**](stores/40a07b89-bc4a-4339-aeaa-e7336a5b42c9)
    - [**Services**](stores/a2fb6726-907f-39ed-b17c-03b3a7f460db)
      - [**Dashboard**](stores/5b73c48f-50ad-4a09-aa27-b81dcc4b4238)
  - [**Shell environments**](stores/7f1a8806-7076-3b72-9f14-806fe0db849c)
    - [**bash**](stores/fc766e9e-f7f6-4870-8eca-0a83b3350830)
    - [**dash**](stores/51eb8f89-c0d2-402b-bd5f-a1c88baba76b)
- [**lappy**](stores/5f0946ba-3c68-4a4c-b149-fd21942da438)
  - [**Proxmox systems**](stores/fb7ed1e5-09de-45c2-9f13-38a87df5fc48)
    - [**debian**](stores/fd38cf00-8bc5-4508-9b14-85c5ef27047a)
    - [**GhostHAS-1337**](stores/2e01d428-3140-4a4f-a310-780c98ac975d)
    - [**influxdb**](stores/659a98ee-45f9-4a7a-b0c1-1d180153ac9d)
    - [**pdc**](stores/433bae5e-e592-437f-9ce3-add2d40c895a)
    - [**Services**](stores/39e0302c-db0c-3f3e-bf9e-edbddf541062)
      - [**Dashboard**](stores/012626ff-8cd8-42be-9143-1ca1f558612a)
    - [**urbackup**](stores/12f9d68c-ef6a-47fb-8a6e-3dc48a311f43)
    - [**window**](stores/02cd869a-ba91-412b-8388-ab0aafd493a6)
  - [**Shell environments**](stores/236a9fe2-32ea-33f0-8a19-5cc6128075fb)
    - [**bash**](stores/c4519fc1-2cd5-4800-b983-eb0d00012d75)
    - [**dash**](stores/ca8f524f-85a9-45e0-872b-117358dfee29)
- [**radios**](stores/b90b2e34-3c3a-47c4-959e-25dc69addfb7)
  - [**Shell environments**](stores/ff09790f-deae-375e-9235-d17765ae0ced)
    - [**bash**](stores/57d7b2f5-4940-410d-9a7c-783303e206e2)
    - [**dash**](stores/d664db91-1e4a-4c19-92ac-1e3efc428973)
- [**servarr**](stores/46ef32ea-4a55-40ff-8b4d-688185c2578f)
  - [**servarr**](stores/5e878fba-c3b5-4e7d-aad3-3eee9c247652)
    - [**deb-tempate**](stores/288d5868-4436-4a2d-bbc7-1aef90f3371b)
    - [**docker-servarr**](stores/45497bd5-66ec-4965-a9ac-df4ba57695ce)
    - [**influxdb**](stores/71de2bee-23a0-43d7-b3b9-61f23e6c6708)
    - [**plex-lxc**](stores/e4fbf58d-eb09-411a-873b-734c37e378bf)
    - [**Services**](stores/3be465ab-4e49-3b3a-babf-d5f009af8226)
      - [**Dashboard**](stores/626efae2-dd0d-449f-837b-1ba2b9943759)
    - [**TrueNasScale**](stores/debaf8be-9e0e-44ff-a544-6b109f0a627a)
    - [**urbackup**](stores/799e0195-c960-468e-b195-9d67f6e0ac45)
    - [**window**](stores/4078e2fd-0149-4061-a03b-aee18d5d0f6b)
    - [**window**](stores/7825fcf1-b969-49c2-b88e-a4e86d10eadf)
  - [**Shell environments**](stores/b3a84a9d-cc7d-32cc-8c93-d3bbe78bfde8)
    - [**bash**](stores/8107881d-1601-4f87-b27c-fb69bda5128b)
    - [**dash**](stores/d57b3ea0-831c-450e-9d40-1374812d9e8d)

**All identities / Synced**

empty


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
