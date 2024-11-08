# Convert Markdown to RTL HTML using Pandoc

Welcome to the **Pandoc Markdown to RTL HTML** guide! 🎉 This guide will show you how to transform your Markdown files into stunning right-to-left (RTL) HTML files using Pandoc. Let's get started!

## Prerequisites 🛠️

Before we dive in, make sure you have the following:

- [Pandoc](https://pandoc.org/installing.html) installed on your system.
- A Markdown file ready for conversion.

## Installation 🚀

### Windows 🪟

1. Grab the Pandoc installer from the [Pandoc releases page](https://github.com/jgm/pandoc/releases).
2. Run the installer and follow the on-screen instructions. Easy peasy!

### macOS 🍏

1. Install Pandoc using Homebrew:

  ```sh
  brew install pandoc
  ```

### Linux 🐧

Install Pandoc using your package manager. For example, on Debian-based systems:

```sh
sudo apt-get install pandoc
```

## Usage 🎨

To convert a Markdown file to an RTL HTML file, use this magical command:

```sh
pandoc input.md -o output.html  --embed-resources --standalone --css=rtl.css
```

### Explanation 📖

- `input.md`: Your Markdown masterpiece.
- `-o output.html`: The resulting HTML file.
- `--self-contained`: Ensures the HTML file is self-contained, embedding all resources.
- `--css=rtl.css`: Points to a CSS file with RTL styles.

### Example 📝

Create a CSS file named `rtl.css` in the same directory with the following content:

```css
/* General styles for the document */
body {
  font-family: 'XB Niloofar', sans-serif;
  direction: rtl;
  text-align: right;
  line-height: 1.6;
  margin: 20px;
  background-color: #121212; /* Dark background */
  color: #e0e0e0; /* Light text color */
}

/* Styles for headers */
h1, h2, h3, h4, h5, h6 {
  text-align: right;
  color: #ffffff; /* White text for headers */
}

/* Styles for paragraphs */
p {
  text-align: right;
  color: #e0e0e0; /* Light text color */
}

/* Styles for lists */
ul, ol {
  text-align: right;
  padding-right: 20px;
  color: #e0e0e0; /* Light text color */
}

/* Styles for code blocks and plaintext */
pre, code, .plaintext {
  direction: ltr;
  text-align: left;
  font-family: 'Courier New', Courier, monospace;
  background-color: #333333; /* Dark background for code blocks */
  color: #e0e0e0; /* Light text color */
  padding: 10px;
  border-radius: 5px;
  overflow-x: auto;
}

/* Styles for inline code */
code {
  background-color: #333333; /* Dark background for inline code */
  color: #e0e0e0; /* Light text color */
  padding: 2px 4px;
  border-radius: 3px;
}

/* Styles for blockquotes */
blockquote {
  border-right: 5px solid #444444; /* Dark border for blockquotes */
  padding-right: 10px;
  margin-right: 20px;
  color: #aaaaaa; /* Light gray text for blockquotes */
}

/* Styles for tables */
table {
  width: 100%;
  border-collapse: collapse;
  margin-bottom: 20px;
  background-color: #1e1e1e; /* Dark background for tables */
  color: #e0e0e0; /* Light text color */
}

th, td {
  border: 1px solid #444444; /* Dark border for table cells */
  padding: 8px;
  text-align: right;
}

th {
  background-color: #333333; /* Dark background for table headers */
  color: #e0e0e0; /* Light text color */
}
```

Run the Pandoc command:

```sh
pandoc input.md -o output.html  --embed-resources --standalone --css=rtl.css
```

Voilà! You've got yourself a beautiful RTL HTML file named `output.html`.

## Conclusion 🎉

By following these steps, you can effortlessly convert a Markdown file to an RTL HTML file using Pandoc. Feel free to tweak the CSS to match your style. Happy converting! 🚀
