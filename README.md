# 📧 React Mailer

**Free email configuration tool for React applications**

Generate a complete PHP backend and React hook for sending emails from your forms. No external dependencies, no monthly fees, works with any hosting provider's SMTP.

🌐 **[Try it now → Live Demo](https://alfredo-villa.github.io/react-mailer)**

---

## ✨ Features

- 🆓 **100% Free** - No paid services required
- 🔒 **Secure** - Token authentication, rate limiting, honeypot anti-bot
- 🌍 **Multilingual** - English, Italian, Spanish, French
- ⚡ **Zero Dependencies** - Pure PHP backend, no composer packages
- 📧 **HTML Emails** - Beautiful responsive email templates
- 🎯 **30+ Presets** - Quick configuration for popular hosting providers
- 🔐 **Privacy First** - Runs 100% in your browser, no data sent anywhere

---

## 🚀 How It Works

1. **Open the tool** at [alfredo-villa.github.io/react-mailer](https://alfredo-villa.github.io/react-mailer)
2. **Select your hosting** provider or enter SMTP details manually
3. **Fill in** your domain and recipient email
4. **Download** the generated files (mailer.php, mailer-config.php, useMailer.js)
5. **Upload** PHP files to your server's `/api/` folder
6. **Use** the React hook in your components

---

## 📁 Generated Files

| File | Description |
|------|-------------|
| `mailer.php` | PHP backend (~200 lines) - handles SMTP sending |
| `mailer-config.php` | Configuration with your credentials |
| `useMailer.js` | React hook for easy integration |
| `README.md` | Quick start guide with your settings |
| `.env.example` | Environment variables template |

---

## 💻 Usage in React

```jsx
import { useMailer } from './hooks/useMailer';

function ContactForm() {
  const { sendEmail, loading, error, success } = useMailer(
    'https://yourdomain.com/api/mailer.php',
    'YOUR_GENERATED_TOKEN'
  );

  const handleSubmit = async (e) => {
    e.preventDefault();
    await sendEmail({
      fields: { 
        email: 'user@example.com', 
        message: 'Hello!',
        website: '' // honeypot field
      }
    });
  };

  return (
    <form onSubmit={handleSubmit}>
      {/* Your form fields */}
      <button disabled={loading}>
        {loading ? 'Sending...' : 'Send'}
      </button>
      {error && <p className="error">{error}</p>}
      {success && <p className="success">Sent!</p>}
    </form>
  );
}
```

---

## 🔧 Supported Hosting Providers

### Europe
Aruba, IONOS, OVH, Hetzner, Strato, Infomaniak, Register.it, Netsons

### Americas
GoDaddy, Bluehost, HostGator, DreamHost, Namecheap, A2 Hosting, InMotion

### Global
SiteGround, Hostinger, Cloudways, cPanel, Plesk

### Email Services
Gmail, Outlook/O365, Yahoo, Zoho Mail, SendGrid, Mailgun, Amazon SES, Postmark

---

## 🔐 Security Features

| Feature | Description |
|---------|-------------|
| **Token Auth** | Every request requires a secret token |
| **Rate Limiting** | 5 emails/hour per IP (configurable) |
| **Honeypot** | Hidden field to catch bots |
| **CORS** | Only allowed domains can send requests |
| **Input Validation** | Email format and required fields |
| **Logging** | All attempts are logged with IP |

---

## 🌐 Browser Support

Works in all modern browsers:
- Chrome, Firefox, Safari, Edge (latest versions)
- No server-side processing - everything runs locally in your browser

---

## 📝 License

MIT License - Free for personal and commercial use.

---

## 🤝 Contributing

Contributions are welcome! Feel free to:
- Report bugs
- Suggest new features
- Add more hosting presets
- Improve translations

---

## ☕ Support

If this tool saved you time, consider buying me a coffee:

[![PayPal](https://img.shields.io/badge/PayPal-Donate-blue?style=for-the-badge&logo=paypal)](https://paypal.me/valfredo8)

---

## 👤 Author

**Alfredo Villa**

- GitHub: [@alfredovilla](https://github.com/alfredo-villa)

---

<p align="center">
  Made with ❤️ for the developer community
</p>
