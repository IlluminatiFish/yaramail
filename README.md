<div>
  <img src="https://seanthegeek.github.io/yaramail/_static/yaramail-logo.png" style="padding-top: 10px; display:block;float:none;margin-left:auto;margin-right:auto;" alt="yaramail logo">
<h1 style="text-align: center;">yaramail</h1>

  [![Python tests](https://github.com/seanthegeek/yaramail/actions/workflows/python-tests.yaml/badge.svg)](https://github.com/seanthegeek/yaramail/actions/workflows/python-tests.yaml)
  [![PyPI](https://img.shields.io/pypi/v/yara-mail)](https://pypi.org/project/yara-mail/)
  [![PyPI - Downloads](https://img.shields.io/pypi/dm/yara-mail?color=blue)](https://pypistats.org/packages/yara-mail)
</div>

`yaramail` is a Python package and command line utility for scanning emails with
[YARA rules][yara]. It is Ideal for automated triage of phishing reports.

## Features

- Scans all parts of an email via API or CLI
  - Headers
    - Removes header indents by default for consistent scanning
  - Plain text and HTML body content
    - Converts body content to Markdown by default for consistent scanning
  - Attachments
    - Raw file content
    - Emails attached to emails
    - PDF document text
    - ZIP file contents, including nested ZIP files
      - Uses message body content as a list of possible ZIP passwords
      - Customizable list of passwords to use when attempting to scan encrypted ZIP files
- Provides a built-in methodology for categorizing emails
- Parses `Authentication-Results` headers

[yara]: https://yara.readthedocs.io/en/stable/writingrules.html
