
Upload an app file to a build
-----------------------------

### Endpoint

    POST /api/v2/app_files

### Parameters

<table border="1" class="nice">
<tbody><tr>
  <th>Name</th>
  <th>Description</th>
</tr>
<tr>
  <th>build_id</th>
  <td><ul>
      <li>id of the build (found at the end of the build page url - build must be passed/bypassed testing but not yet released)</li>
    </ul>
  </td>
</tr>
<tr>
  <th>file</th>
  <td><ul>
      <li>file to upload</li>
    </ul>
  </td>
</tr>

</tbody></table>

### Request

#### Headers

    Authorization: Token token=b2a7e8daf78acc517fd65fa43c915b52

#### Body

    ------------XnJLe9ZIbbGUYtzPQJ16u1
    Content-Disposition: form-data; name="build_id"

    1
    ------------XnJLe9ZIbbGUYtzPQJ16u1
    Content-Disposition: form-data; name="file"; filename="test.ipa"
    Content-Type: text/plain
    Content-Length: 224096

    [uploaded data]
    ------------XnJLe9ZIbbGUYtzPQJ16u1--

#### cURL

    curl "https://example.com/api/v2/app_files" -F "build_id=1" -F "file=@path/to/file/test.ipa" -X POST \
        -H "Authorization: Token token=b2a7e8daf78acc517fd65fa43c915b52"

### Response

#### Status

    201

#### Body

    {
      "id": 1,
      "build_id": 1,
      "url": "/resource_files/1",
      "name": "test.ipa",
      "extension": ".ipa",
      "resource_file": true,
      "resource_type": 0,
      "created_at": "25 Feb 06:57 PM",
      "uploader": null,
      "ios_provision_check": true,
      "ios_version_check": true,
      "ios_enable_install": true,
      "ios_enterprise_provision": true,
      "is_beta": false,
      "install_url": "itms-services://?action=download-manifest&amp;url=http%3A%2F%2F10.74.5.147%3A3000%2Fapi%2Fgenerate_manifest%2Fcom_xtremelabs_studio_Xtreme-Rest-Sample%2F1_0%2FXtreme-Rest-Sample%3Fminimum_os_version%3D6_1%26url%3Dhttp%253A%252F%252F10.74.5.147%253A3000%252Fresource_files%252F1%3Fauth_token%3Db2a7e8daf78acc517fd65fa43c915b52",
      "download_url": "/resource_files/1",
      "was_downloaded_by": [

      ],
      "version_num": "1.0"
    }
