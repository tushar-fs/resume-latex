# 📄 Professional LaTeX Resume Template

A clean, modern, and ATS-friendly LaTeX resume template designed for software engineers and tech professionals.

## 📋 Resume Preview

<!-- The compiled PDF will be displayed here -->

![Resume Preview](resume.pdf)

> **📥 [Download PDF](resume.pdf)** | **🔗 [View Source](resume.tex)**

---

## ✨ Features

- **🎯 ATS-Friendly**: Optimized for Applicant Tracking Systems
- **📱 Clean Design**: Professional, modern layout with proper spacing
- **🔧 Easy Customization**: Well-commented code for quick modifications
- **📊 Structured Sections**: Education, Experience, Projects, Technologies
- **🎨 Professional Icons**: FontAwesome icons for contact information
- **⚡ Fast Compilation**: Minimal dependencies, quick builds

---

## 🚀 Quick Start

### Prerequisites

You'll need LaTeX installed on your system:

#### macOS

```bash
# Install MacTeX (recommended)
brew install --cask mactex

# Or install BasicTeX (smaller)
brew install --cask basictex
```

#### Windows

```bash
# Install MiKTeX
winget install MiKTeX.MiKTeX
```

#### Linux (Ubuntu/Debian)

```bash
sudo apt-get install texlive-full
```

### Compile the Resume

```bash
# Clone the repository
git clone <your-repo-url>
cd resume

# Compile LaTeX to PDF
pdflatex resume.tex

# Open the generated PDF
open resume.pdf  # macOS
start resume.pdf # Windows
xdg-open resume.pdf # Linux
```

---

## 🛠️ Customization Guide

The template is designed to be easily customizable. Look for `% CHANGE:` comments in the code.

### 📝 Personal Information

```latex
% Header section - Replace with your information
\fontsize{25 pt}{25 pt}\selectfont Your Name Here  % CHANGE: Your full name

% Contact information
\mbox{\faEnvelope\ \hrefWithoutArrow{mailto:your.email@domain.com}{your.email@domain.com}}
\mbox{\faPhone\ \hrefWithoutArrow{tel:+1-xxx-xxx-xxxx}{+1 (xxx) xxx-xxxx}}
\mbox{\faLinkedin\ \hrefWithoutArrow{https://linkedin.com/in/your-profile}{your-profile}}
\mbox{\faGithub\ \hrefWithoutArrow{https://github.com/your-username}{your-username}}
```

### 🎓 Education Section

```latex
% Education format
\textbf{University Name} \hfill {\color{darkgray}\small{\textbf{Start Date – End Date} $|$ Location}}\\
{\color{darkgray}\textit{Degree Title}} $|$ \textit{GPA: X.X/4.0}
```

### 💼 Experience Section

```latex
% Experience format
\textbf{Job Title}, {\color{darkgray}\textit{Company Name}} \hfill {\color{darkgray}\small{\textbf{Start Date – End Date} $|$ Location}}
```

### 🚀 Projects Section

```latex
% Project format
\textbf{Project Name [\textit{Description}]} \hfill \href{https://github.com/username/repo}{\small \faGithub \space GitHub}
```

---

## 🎨 Customization Options

### Font Changes

The template uses Charter font by default. To change fonts:

```latex
% Current font
\usepackage{charter}

% Alternative fonts (uncomment one):
% \usepackage{mathptmx}       % Times New Roman
% \usepackage{palatino}       % Palatino
% \usepackage{helvet}         % Helvetica
% \usepackage{lmodern}        % Latin Modern
```

### Color Scheme

Modify colors by changing RGB values:

```latex
% Primary color for links
\definecolor{primaryColor}{RGB}{0, 0, 0}        % Black (default)

% Dark gray for dates and locations
\definecolor{darkgray}{rgb}{0.2, 0.2, 0.2}      % Dark gray (default)

% Example color alternatives:
% \definecolor{primaryColor}{RGB}{0, 100, 200}   % Blue
% \definecolor{primaryColor}{RGB}{150, 0, 0}     % Dark red
```

### Margins and Spacing

Adjust page margins:

```latex
\usepackage[
    top=1.0 cm,         % Top margin
    bottom=1.0 cm,      % Bottom margin
    left=1.0 cm,        % Left margin
    right=1.0 cm,       % Right margin
    footskip=1.0 cm     % Footer spacing
]{geometry}
```

---

## 📁 File Structure

```
.
├── resume.tex          # Main LaTeX source file
├── resume.pdf          # Compiled PDF (generated)
├── README.md           # This documentation
└── .gitignore          # Git ignore file
```

---

## 🔧 Advanced Customization

### Adding New Sections

To add a new section, follow this pattern:

```latex
\section{New Section Title}

    \noindent
    \textbf{Item Title} \hfill {\color{darkgray}\small{\textbf{Date Range} $|$ Location}}

    \begin{highlights}
        \item Your first bullet point
        \item Your second bullet point
    \end{highlights}
```

### Modifying List Spacing

Adjust bullet point spacing in the `highlights` environment:

```latex
\newenvironment{highlights}{
    \begin{itemize}[
        topsep=0.10 cm,     % Space above the list
        parsep=0.10 cm,     % Space between paragraphs
        itemsep=0pt,        % Space between items
        leftmargin=10pt     % Left margin for bullets
    ]
}{
    \end{itemize}
}
```

---

## 📚 Dependencies

The template uses these LaTeX packages:

- `geometry` - Page layout and margins
- `titlesec` - Section title formatting
- `xcolor` - Color support
- `fontawesome5` - Icons for contact info
- `hyperref` - Clickable links
- `enumitem` - List customization
- `paracol` - Multi-column layouts

---

## 💡 Tips for Best Results

1. **Keep it concise**: Aim for 1-2 pages maximum
2. **Use action verbs**: Start bullet points with strong action words
3. **Quantify achievements**: Include numbers and percentages when possible
4. **Tailor for each job**: Customize skills and experience for the role
5. **Test ATS compatibility**: Ensure the PDF is text-searchable

---

## 🐛 Troubleshooting

### Common Issues

**LaTeX not found:**

```bash
# Make sure LaTeX is in your PATH
echo $PATH
# Add LaTeX to PATH if needed (macOS)
export PATH="/usr/local/texlive/2024/bin/universal-darwin:$PATH"
```

**Missing packages:**

```bash
# Install missing packages (MacTeX)
tlmgr install [package-name]

# Update all packages
tlmgr update --all
```

**PDF not generating:**

- Check for LaTeX syntax errors in the output
- Ensure all `\begin{}` have matching `\end{}`
- Verify file permissions in the directory

---

## 📄 License

This template is open source and available under the [MIT License](LICENSE).

---

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

## 📧 Contact

**Tushar Singh**

- 📧 Email: connect.tushar0@gmail.com
- 💼 LinkedIn: [tushar-singh-sde](https://linkedin.com/in/tushar-singh-sde)
- 🐙 GitHub: [tushar-fs](https://github.com/tushar-fs)

---

**⭐ If this template helped you land your dream job, please consider giving it a star!**
