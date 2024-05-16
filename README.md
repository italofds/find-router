# find-router

This tool receives the MAC address of a Wi-Fi access point and queries a geolocation database to present its geographical position on an interactive map. It provides a precise and quick visualization, making it ideal for tracking and analyzing network devices.

## Key Features

- **Router Location Query:** Provides geolocation information for Wi-Fi access points in a simple and clear way.
- **User-Friendly Design:** Designed with a focus on ease of use, making it easy to consult and display results.
- **Easy Setup:** Simplified configuration for quick deployment and use in various development environments.

## Prerequisites

Before starting using the **find-router** application, it is necessary to have Node.js installed on your machine. Additionally, it is also necessary to have a valid Google Geolocation API key, which must be configured in the `.env.development` file.

## Installation and Configuration

1. Clone the project repository to your local machine:

```bash
git clone https://github.com/italofds/find-router.git
cd find-router
```

2. Install the project dependencies:

```bash
npm install
```

3. Start the WEB application to send querys:

```bash
vue serve
```

## Usage

After setup, the WEB application is ready to be used. To perform a query, simply access the application through your preferred browser, informing the local address:

http://localhost:8080
 
Further usage instructions will be available on the application's own home page.

## Deploy

For deploying the Vue.js project, the following command should be executed:

```bash
npm run build:prod
```

After doing so, all the deployment content will be available in the `dist` folder.

## Contributing

Contributions to **find-router** are always welcome. Whether it's adding support for new Geolocation APIs, improving the application's usability, suggesting new features, or documenting the project, your help is valuable in making this tool even more powerful.

## License

This project is licensed under the GNU General Public License (GPL), a free software license that guarantees users the freedom to run, study, share, and modify the software.

The GPL is a copyleft license, which means that any modified versions of the software must also be distributed under the same terms of the license. This promotes a free software community, encouraging collaboration and the sharing of improvements.

For more information about the GPL and its terms and conditions of use, visit [GNU General Public License](https://www.gnu.org/licenses/gpl-3.0.html).