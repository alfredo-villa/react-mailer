# Contributing to React Mailer

Thank you for your interest in contributing! 🎉

## How to Contribute

### Report Bugs
- Open an issue describing the bug
- Include browser/OS information
- Provide steps to reproduce

### Suggest Features
- Open an issue with the "feature request" label
- Describe the feature and its use case

### Add Hosting Presets
Want to add a new hosting provider? Edit `index.html` and add to the `presets` object:

```javascript
presets = {
    // ... existing presets
    newprovider: { host: 'smtp.newprovider.com', port: '587' },
};
```

Then add the button in the HTML:
```html
<button class="preset-btn" onclick="fillPreset('newprovider')">NewProvider</button>
```

### Improve Translations
Translations are in the `i18n` object in `index.html`. Add or improve translations for:
- English (en)
- Italian (it)
- Spanish (es)
- French (fr)
- Or add a new language!

### Code Style
- Keep it simple and readable
- No external dependencies (except JSZip for downloads)
- Test in multiple browsers before submitting

## Pull Request Process

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## Questions?

Feel free to open an issue for any questions!
