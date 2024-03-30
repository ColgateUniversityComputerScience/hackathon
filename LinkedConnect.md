
# LinkedConnect

Programmatically search profiles, send messages, and find jobs using a regular LinkedIn user account.

**Caution**: This library is unofficial and might violate LinkedIn's Terms of Service. Use it at your own risk.

## Installation

**Requirements:** Python >= 3.6

To install the `LinkedConnect` package, use the following command:

```bash
pip install linkedconnect
```

For the bleeding-edge version, use:

```bash
pip install git+https://github.com/your-github/linkedconnect.git
```

## Quick Start

Refer to the [official documentation](https://linkedconnect.readthedocs.io/) for all methods.

Example usage:

```python
from linkedconnect import LinkedConnect

# Authenticate using LinkedIn account credentials
api = LinkedConnect('email@example.com', 'password')

# GET a profile
profile = api.get_profile('profile-id')

# GET profile contact info
contact_info = api.get_profile_contact_info('profile-id')

# GET 1st degree connections of a profile
connections = api.get_profile_connections('profile-id')
```

## Documentation

For comprehensive documentation, including available methods and parameters, visit the [documentation website](https://linkedconnect.readthedocs.io/).

## Commercial Alternatives

This section is sponsored.

- **[Prospeo](https://prospeo.io/api/linkedin-email-finder)**: Real-time data extraction and email verification.
- **[Proxycurl](https://nubela.co/proxycurl/)**: Scalable LinkedIn profile data scraping.

For more details, check the links provided in the sponsors' section above.

## Disclaimer

This library is not endorsed or supported by LinkedIn. It is intended for educational and personal use only. Users should comply with LinkedIn's Terms of Service.

## Contributing

Contributions are welcome! Check out the contribution guidelines.

## Development

**Dependencies:**
- Python 3.7
- A valid LinkedIn user account (not personal, if possible)
- `pipenv` (optional)

**Setting up:**

1. Clone the repository and navigate into it.
2. Create a `.env` file based on `.env.example`.
3. Install dependencies:

```bash
pipenv install --dev
pipenv shell
```

**Run tests:**

```bash
pipenv run test
```

## Troubleshooting

For issues like `CHALLENGE` prompts or search problems, refer to the troubleshooting section.

## How It Works

The LinkedConnect API interfaces with LinkedIn's internal Voyager service to retrieve data available on linkedin.com.

### Deep Dive into Voyager

Voyager is accessed via endpoints authenticated with a user's cookie. Details on finding new endpoints and how LinkedIn's clients query Voyager are included in the deep dive section.

## Contact Information

For further assistance or inquiries, contact:

- Name: [Isaiah Cerven]
  - Email: [icerven@colgate.edu](mailto:icerven@colgate.edu)

## GitHub Repository

Access my project's source code on GitHub: [LinkedConnect Repository](https://github.com/CerIsaiah/LinkedConnect.git)
