# TestSdk Python SDK 1.0.0

Welcome to the TestSdk SDK documentation. This guide will help you get started with integrating and using the TestSdk SDK in your project.

## Versions

- API version: `1.0.0`
- SDK version: `1.0.0`

## Table of Contents

- [Setup & Configuration](#setup--configuration)
  - [Supported Language Versions](#supported-language-versions)
  - [Installation](#installation)
- [Authentication](#authentication)
  - [Access Token Authentication](#access-token-authentication)
- [Setting a custom Timeout](#setting-a-custom-timeout)
- [Sample Usage](#sample-usage)
- [Services](#services)
- [Models](#models)
- [License](#license)

## Setup & Configuration

### Supported Language Versions

This SDK is compatible with the following versions: `Python >= 3.7`

### Installation

To get started with the SDK, we recommend installing using `pip`:

```bash
pip install test_sdk
```

## Authentication

### Access Token Authentication

The TestSdk API uses an Access Token for authentication.

This token must be provided to authenticate your requests to the API.

#### Setting the Access Token

When you initialize the SDK, you can set the access token as follows:

```py
TestSdk(
    access_token="YOUR_ACCESS_TOKEN",
    timeout=10000
)
```

If you need to set or update the access token after initializing the SDK, you can use:

```py
sdk.set_access_token("YOUR_ACCESS_TOKEN")
```

## Setting a custom Timeout

You can set a custom timeout for the SDK's HTTP requests as follows:

```py
from test_sdk import TestSdk

sdk = TestSdk(timeout=10000)
```

# Sample Usage

Below is a comprehensive example demonstrating how to authenticate and call a simple endpoint:

```py
from test_sdk import TestSdk, Environment

sdk = TestSdk(
    access_token="YOUR_ACCESS_TOKEN",
    base_url=Environment.DEFAULT.value,
    timeout=10000
)

result = sdk.pets.list_pets(limit=81)

print(result)

```

## Services

The SDK provides various services to interact with the API.

<details> 
<summary>Below is a list of all available services with links to their detailed documentation:</summary>

| Name                                                 |
| :--------------------------------------------------- |
| [PetsService](documentation/services/PetsService.md) |

</details>

## Models

The SDK includes several models that represent the data structures used in API requests and responses. These models help in organizing and managing the data efficiently.

<details> 
<summary>Below is a list of all available models with links to their detailed documentation:</summary>

| Name                               | Description |
| :--------------------------------- | :---------- |
| [Pet](documentation/models/Pet.md) |             |

</details>

## License

This SDK is licensed under the MIT License.

See the [LICENSE](LICENSE) file for more details.

<!-- This file was generated by liblab | https://liblab.com/ -->
