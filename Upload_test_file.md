[App Distribution](/docs) {.navbar-brand}
=========================

[README](/docs)

[Builds](/docs/builds/bypass_testing_for_a_build)

-   [Bypass testing for a
    build](/docs/builds/bypass_testing_for_a_build)
-   [Creating a build](/docs/builds/creating_a_build)
-   [Release a build for
    testing](/docs/builds/release_a_build_for_testing)
-   [Share a build](/docs/builds/share_a_build)

[Files](/docs/files/upload_a_test_file_to_a_build)

-   [Upload a test file to a
    build](/docs/files/upload_a_test_file_to_a_build)
-   [Upload an app file to a
    build](/docs/files/upload_an_app_file_to_a_build)

[Notes](/docs/notes/creating_release_notes_for_a_build)

-   [Creating release notes for a
    build](/docs/notes/creating_release_notes_for_a_build)
-   [Creating testing notes for a
    build](/docs/notes/creating_testing_notes_for_a_build)

Files {.resource-name}
=====

Upload a test file to a build
-----------------------------

### Endpoint

    POST /api/v2/test_files

### Parameters

  Name                 Description
  -------------------- ----------------------------------------------------------
  build\_id required   The id of the build (release id from the build page url)
  file                 The file to upload

### Request

#### Headers

    Authorization: Token token=7843fb86003e50ed88552efaeecb5d83

#### Body

    ------------XnJLe9ZIbbGUYtzPQJ16u1
    Content-Disposition: form-data; name="build_id"

    1
    ------------XnJLe9ZIbbGUYtzPQJ16u1
    Content-Disposition: form-data; name="file"; filename="test.apk"
    Content-Type: text/plain
    Content-Length: 233331

    [uploaded data]
    ------------XnJLe9ZIbbGUYtzPQJ16u1--

#### cURL

    curl "https://example.com/api/v2/test_files" -F "build_id=1" -F "file=@path/to/file/test.apk" -X POST \
        -H "Authorization: Token token=7843fb86003e50ed88552efaeecb5d83"

### Response

#### Status

    201

#### Body

    {
      "id": 1,
      "build_id": 1,
      "url": "/resource_files/1",
      "name": "test.apk",
      "extension": ".apk",
      "resource_file": true,
      "resource_type": 1,
      "created_at": "25 Feb 06:57 PM",
      "uploader": null,
      "ios_provision_check": true,
      "ios_version_check": true,
      "ios_enable_install": true,
      "ios_enterprise_provision": false,
      "is_beta": false,
      "install_url": "http://10.74.5.147:3000/resource_files/1",
      "download_url": "/resource_files/1",
      "was_downloaded_by": [

      ],
      "version_num": "1"
    }
