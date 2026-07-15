```
Project Objective
```

```
Describe and design an application to securely interact with the Google Gemini
API from the command-line to analyze files, classify them into vulnerability
categories, and
```

```
provide color-coded severity reports.
```

```
{Required Tools}
```

```
Python 3
Google Generative AI SDK
PowerShell
Cursor
```

```
---
```

```
Technical Implementation Summary:
Cursor was isolated in a virtual development environment (venv) to prevent
packages from the different projects from interfering with each other.
Environment variables are used to maintain developer keys in isolation, and
secure integration with the Google Gemini API was constructed. It is constructed
secure integration with Google Gemini API, and the developer keys are kept in
isolation through environment variables. A script for targeted static analysis
was developed to take code base parameters, feed dynamic payloads and generate
back security threat analysis in the form of a report. The script can interpret
the response to the security request and correlate the Colorama formatting codes
to Terminology criticality levels (Critical, High, Medium, Low) and output the
warning block in color to the console.
```

```
---
```

```
{Operational Relevance}
```

```
Application Security & Threat Detection:
```

```
I tested the tool with copies of files that deliberately had vulnerabilities.
The small script tool worked well for me to cause high contrast console
warnings.
```

```
API Integration & Secure Software Supply Chain:
```

```
I created a clean interface that uses the Google Gemini API and kept developer
credentials isolated with the help of environment files (.env). This means there
are never any secrets in shared code itself, similar to how companies securely
integrate APIs in their applications.
```

```
Scripting Automation & Operational Efficiency:
```

```
Worked with the development pipeline in a clean virtual environment and updated
execution parameters in PowerShell. This highlighted my ability to develop,
deploy, and solve problems with automated scripts.
```

