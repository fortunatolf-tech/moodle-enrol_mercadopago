# Moodle Enrollment MercadoPago

![Moodle Plugin](https://img.shields.io/badge/Moodle-Plugin-orange?style=flat&logo=moodle)
![PHP](https://img.shields.io/badge/PHP-7.4+-777BB4?style=flat&logo=php&logoColor=white)
![License](https://img.shields.io/badge/License-GPL--3.0-blue.svg)
![Stars](https://img.shields.io/github/stars/harregoces/moodle-enrol_mercadopago?style=social)

A Moodle enrollment plugin that enables course payments through **MercadoPago** payment gateway, supporting multiple Latin American countries.

## Features

- Seamless integration with MercadoPago payment gateway
- Support for multiple currencies (ARS, BRL, CLP, COP, MXN, PEN, UYU)
- Automatic enrollment upon successful payment
- Email notifications for students, teachers, and admins
- Sandbox mode for testing
- Configurable enrollment duration
- Role assignment on enrollment

## Supported Countries

| Country | Currency |
|---------|----------|
| Argentina | ARS |
| Brazil | BRL |
| Chile | CLP |
| Colombia | COP |
| Mexico | MXN |
| Peru | PEN |
| Uruguay | UYU |

## Screenshots

### Plugin Settings
![Settings Screenshot](pix/screenshot.png "Plugin Settings")

### Course Enrollment Settings
![Course Settings](pix/screenshot2.png "Course Enrollment Settings")

### Payment Page
![Payment Page](pix/screenshot3.png "Payment Page")

## Requirements

- Moodle 3.5 or higher
- PHP 7.4 or higher
- MercadoPago account with API credentials

## Installation

### Via Git (Recommended)

```bash
cd /path/to/moodle/enrol
git clone https://github.com/harregoces/moodle-enrol_mercadopago.git mercadopago
```

### Manual Installation

1. Download the latest release
2. Extract the contents
3. Copy the `mercadopago` folder to `/path/to/moodle/enrol/`
4. Visit Site Administration > Notifications to complete the installation

## Configuration

1. Go to **Site Administration > Plugins > Enrolments > Manage enrol plugins**
2. Enable "MercadoPago" enrollment
3. Click on "Settings" to configure the plugin
4. Enter your MercadoPago Access Token
5. Configure notification settings as needed

### Sandbox Testing

For testing in sandbox mode, add these lines to your `config.php`:

```php
$CFG->usemercadopagosandbox = true;
$CFG->mercadopagosandbox_email = 'test_user@testuser.com';
```

Generate test users at: [MercadoPago Test Users](https://www.mercadopago.com.co/developers/en/guides/qr-code/final-steps/integration-test/)

## Usage

1. Navigate to the course you want to enable payments for
2. Go to **Course Administration > Users > Enrolment methods**
3. Add "MercadoPago" from the dropdown
4. Configure the enrollment cost and currency
5. Save changes

Students will see the payment option when they try to enroll in the course.

## Documentation

- [MercadoPago PHP SDK](https://www.mercadopago.com.co/developers/en/guides/sdks/official/php/)
- [MercadoPago API Documentation](https://www.mercadopago.com.co/developers/en/reference)

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## Support

If you find this plugin useful, consider:

- Giving it a star on GitHub
- [Sponsoring on Patreon](https://patreon.com/harregoces)
- [Donating via PayPal](https://paypal.me/harregoces)

## Author

**Hernan Arregoces** - Software Engineer specialized in Moodle Development

- [Moodle Profile](https://moodle.org/user/profile.php?id=1931915)
- [LinkedIn](https://www.linkedin.com/in/hernanarregoces/)
- [GitHub](https://github.com/harregoces)

## License

This project is licensed under the GPL-3.0 License - see the [LICENSE](LICENSE) file for details.

---

Made with love for the Moodle community
