# ponces-priv_keys-template

# Usage

```bash
croot && git clone https://github.com/ponces/vendor_ponces-priv_keys-template vendor/ponces-priv/keys
```

```bash
cd vendor/ponces-priv/keys
```

```
./keys.sh
```

# Testing

Included `check_keys.py` script checks whether all apk/apex/capex files in the build out are signed with keys within its directory. Be aware that some targets are **expected** to be signed with vendor key, for example `com.android.apex.cts.shim.v1_prebuilt`.

```
$ ./check_keys.py ~/aosp/out/target/product/tdgsi_arm64_ab
/home/ponces/aosp/out/target/product/tdgsi_arm64_ab/obj/ETC/com.android.apex.cts.shim.v1_prebuilt_intermediates/com.android.apex.cts.shim.apex is signed with an unknown key!
```
