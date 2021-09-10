# 解决7.0 系统私有目录被限制访问

## AndroidManifest.xml
```
<provider
  android:name="androidx.core.content.FileProvider"
  android:authorities="${applicationId}.fileprovider"
  android:exported="false"
  android:grantUriPermissions="true">
            
  <meta-data
    android:name="android.support.FILE_PROVIDER_PATHS"
    android:resource="@xml/file_paths" />
</provider>
```


## file_paths.xml
```
<?xml version="1.0" encoding="utf-8"?>
<paths>
    <external-files-path
        name="external_file"
        path="." />

    <external-cache-path
        name="external_cache"
        path="." />

    <files-path
        name="files"
        path="." />

    <cache-path
        name="cache"
        path="." />

    <external-path name="external_files" path="." />
</paths>
```
