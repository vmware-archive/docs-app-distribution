

Release a build for testing
---------------------------

### Endpoint

    POST /api/v2/builds/:id/release_for_testing

### Parameters

  Name     Description
  -------- --------------------------
  notify   List of emails to notify

### Request

#### Headers

    Authorization: Token token=dbe05b32726cc67279063a2c1d0b0681
    Content-Type: application/json

#### Body

    {
      "notify": [
        "tester1@example.com",
        "test2@example.com"
      ]
    }

#### cURL

    curl "https://example.com/api/v2/builds/3/release_for_testing" -d '{"notify":["tester1@example.com","test2@example.com"]}' -X POST \
        -H "Authorization: Token token=dbe05b32726cc67279063a2c1d0b0681" \
        -H "Content-Type: application/json"

### Response

#### Status

    200

#### Body

    {
      "id": 3,
      "name": null,
      "project_id": 1,
      "latest_status_string": "Released for Testing",
      "app_files": [

      ],
      "qa_files": [
        {
          "id": 1,
          "build_id": 3,
          "url": "/resource_files/1",
          "name": "test_0.txt",
          "extension": ".txt",
          "resource_file": true,
          "resource_type": 1,
          "created_at": "25 Feb 04:57 PM",
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
          "version_num": null
        }
      ],
      "state": "testing",
      "phase_id": 1,
      "qa_note_id": 1,
      "release_note_id": null,
      "app_build_links": [

      ],
      "qa_build_links": [

      ],
      "created_date": "25 Feb 06:57 PM",
      "is_release_candidate": false,
      "phase_number": 1,
      "qa_release_user": null,
      "qa_approval_user": null,
      "client_release_user": null,
      "bypassed_testing": false,
      "week_number": 1
    }
