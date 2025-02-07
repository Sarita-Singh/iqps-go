<div id="top"></div>
<div align="center">

[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]
[![Wiki][wiki-shield]][wiki-url]

</div>

<br />
<div align="center">
  <a href="https://github.com/metakgp/iqps">
    <img width="140" alt="image" src="https://raw.githubusercontent.com/metakgp/design/main/logos/logo.jpg">
  </a>

  <h3 align="center">IQPS</h3>

  <p align="center">
    <i>Intelligent Question Paper Search</i>
    <br />
    <a href="https://qp.metakgp.org">Website</a>
    ·
    <a href="https://github.com/metakgp/iqps-go/issues">Report Bug / Request Feature</a>
  </p>
</div>

<!-- TABLE OF CONTENTS -->
<details>
<summary>Table of Contents</summary>

- [About The Project](#about-the-project)
- [Development](#development)
- [Deployment](#deployment)
  - [Environment Variables](#environment-variables)
- [Maintainer(s)](#maintainers)
- [Contact](#contact)
- [Additional documentation](#additional-documentation)

</details>

## About The Project
IQPS is a platform for searching and uploading previous year question papers for IIT Kharagpur students. The frontend is deployed at https://qp.metakgp.org and the backend is hosted on a DigitalOcean droplet with 2GB RAM and a single CPU. See [MetaPloy](https://github.com/metakgp/metaploy) for the deployment architecture.

> **NOTE:** Currently in active development. Get involved at our [Slack](https://slack.metakgp.org/).

## Development
1. Clone this repository.
2. Start the backend by running `go run .` in the `backend/` directory.
3. Set up the frontend by running `pnpm install` and then `pnpm start` in the `frontend/` directory.
4. Profit.

### Crawler
[WIP: Steps to locally set up crawler]

## Deployment
### Backend
0. Set up [MetaPloy](https://github.com/metakgp/metaploy) **for production**.
1. Clone this repository at a convenient location such as `/deployments`.
3. `cd backend/`
4. Set the appropriate **production** [environment variables](#environment-variables) in the `.env` file.
5. Run `docker compose up` to start the backend.
6. Optionally set up a Systemd service to start the wiki on startup or use this [deployment github workflow](./.github/workflows/deploy.yaml).

### Environment Variables
Environment variables can be set using a `.env` file. Use the `.env.template` files for reference.

#### Backend
- `DB_PATH`: Path to the database file to use.
- `STATIC_FILES_URL`: The base URL for the static files (PDFs).

#### Frontend
- `VITE_BACKEND_URL`: The IQPS backend URL. Use `http://localhost:5000` in development.

## Maintainer(s)
- [Chirag Ghosh](https://github.com/chirag-ghosh)
- [Rajiv Harlalka](https://github.com/rajivharlalka)
- [Arpit Bhardwaj](https://github.com/proffapt)

<p align="right">(<a href="#top">back to top</a>)</p>

## Contact

<p>
📫 MetaKGP -
<a href="https://bit.ly/metakgp-slack">
  <img align="center" alt="Metakgp's slack invite" width="22px" src="https://raw.githubusercontent.com/edent/SuperTinyIcons/master/images/svg/slack.svg" />
</a>
<a href="mailto:metakgp@gmail.com">
  <img align="center" alt="Metakgp's email " width="22px" src="https://raw.githubusercontent.com/edent/SuperTinyIcons/master/images/svg/gmail.svg" />
</a>
<a href="https://www.facebook.com/metakgp">
  <img align="center" alt="metakgp's Facebook" width="22px" src="https://raw.githubusercontent.com/edent/SuperTinyIcons/master/images/svg/facebook.svg" />
</a>
<a href="https://www.linkedin.com/company/metakgp-org/">
  <img align="center" alt="metakgp's LinkedIn" width="22px" src="https://raw.githubusercontent.com/edent/SuperTinyIcons/master/images/svg/linkedin.svg" />
</a>
<a href="https://twitter.com/metakgp">
  <img align="center" alt="metakgp's Twitter " width="22px" src="https://raw.githubusercontent.com/edent/SuperTinyIcons/master/images/svg/twitter.svg" />
</a>
<a href="https://www.instagram.com/metakgp_/">
  <img align="center" alt="metakgp's Instagram" width="22px" src="https://raw.githubusercontent.com/edent/SuperTinyIcons/master/images/svg/instagram.svg" />
</a>
</p>

<p align="right">(<a href="#top">back to top</a>)</p>

## Additional documentation

- [License](/LICENSE)
- [Code of Conduct](/.github/CODE_OF_CONDUCT.md)
- [Security Policy](/.github/SECURITY.md)
- [Contribution Guidelines](/.github/CONTRIBUTING.md)

<p align="right">(<a href="#top">back to top</a>)</p>

[contributors-shield]: https://img.shields.io/github/contributors/metakgp/iqps-go.svg?style=for-the-badge
[contributors-url]: https://github.com/metakgp/iqps-go/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/metakgp/iqps-go.svg?style=for-the-badge
[forks-url]: https://github.com/metakgp/iqps-go/network/members
[stars-shield]: https://img.shields.io/github/stars/metakgp/iqps-go.svg?style=for-the-badge
[stars-url]: https://github.com/metakgp/iqps-go/stargazers
[issues-shield]: https://img.shields.io/github/issues/metakgp/iqps-go.svg?style=for-the-badge
[issues-url]: https://github.com/metakgp/iqps-go/issues
[license-shield]: https://img.shields.io/github/license/metakgp/iqps-go.svg?style=for-the-badge
[license-url]: https://github.com/metakgp/iqps-go/blob/master/LICENSE
[wiki-shield]: https://custom-icon-badges.demolab.com/badge/metakgp_wiki-grey?logo=metakgp_logo&style=for-the-badge
[wiki-url]: https://wiki.metakgp.org
