# Charles Proxy Certificate Root CA Magisk Module

## Prepare
1. Export pem file from Charles Proxy
2. Get hash of pem file:
    ```shell
    openssl x509 -inform PEM -subject_hash_old -in <pem_file> | head -1
    ```
3. Rename the `pem_file` to its `<hash>.0`
4. Move the `hash_pem_file` to `module/system/etc/security/cacerts`

## Building
```shell
./dist.sh
```

How to release a new version:
1. Push a new tag with a name like `v*`.
2. A new release will be automatically created.

## Usage

1. Download the `.zip` file from the [latest release][latestrelease].
2. Go to *Magisk -> Modules -> Install from storage* and select the downloaded `.zip` file.
3. Reboot.

If a new version comes out, repeat steps 2-4 to update the module.

