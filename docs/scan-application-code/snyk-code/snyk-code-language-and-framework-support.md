# Snyk Code - Supported languages and frameworks

{% hint style="info" %}
For environments supported with other Snyk products, see: [Snyk Open Source - supported languages and package managers](../snyk-open-source/snyk-open-source-supported-languages-and-package-managers/), [Snyk Container - Supported operating system distributions](../../scan-containers/how-snyk-container-works/supported-operating-system-distributions.md), and [Snyk IaC and Cloud - Supported providers](../../scan-cloud-configurations/supported-iac-and-cloud-providers.md).
{% endhint %}

## Language support with Snyk Code AI Engine

Snyk Code is based on a deep-code, semantic-code Analysis Engine, which uses AI to continuously learn from billions of lines of code, and 100s of millions of code fixes, in the global development community. The Snyk Code AI Engine continuously evolves the human-guided reinforced learning cycle lead by Snyk's security researchers and engineers. See [this blog article ](https://snyk.io/blog/advanced-technologies-behind-snyk-code/)for more details.

When files are provided for analysis, the engine determines which file to feed into which parser, in a language-independent common intermediate format. This format preserves and exposes characteristics of the scanned source code.

This technology allows Snyk Code to:

* Support any programming language easily.
* Support multi-language projects, spanning security scans over the different languages.
* Unveil interfile issues, such as issue patterns spread over several source files, which are typically especially hard to track.
* Find issue patterns using the Snyk Code engine, compiling the found issues as a report.

Snyk Code currently supports the following programming languages:

* **C#**
* **C/C++ (Beta)**
* **Go**
* **Java**
* **JavaScript**
* **PHP (currently does not support interfile)**
* **Python**
* **Ruby**
* **TypeScript**
* **Apex**
* **Scala (Beta)**
* **Swift (Beta)**
* **Kotlin (Beta)**
* **VB.NET (Beta)**

{% hint style="info" %}
Beta support exists for Kotlin, Scala and Swift. Contact Snyk for more details or with your further needs.
{% endhint %}

## Language type and framework support

Snyk Code can work with a variety of relevant language types:

* Dynamically typed languages such as JavaScript and Python.
* Optionally strong typed languages such as TypeScript.
* Strong typed languages such as Java.

For a full list of Vulnerability Types/Security Rules that are applied to each supported language by Snyk Code, see [Security Rules used by Snyk Code](security-rules-used-by-snyk-code/).

### Supported Extensions

The following are the supported extensions:

* ejs, es, es6, htm, html, js, jsx, ts, tsx, mjs, cjs, vue, java, erb, haml, rb, rhtml, slim, py, go, ASPX, CS, php, xml, jsp, jspx, cls, c, cc, cpp, cxx, h, hpp, hxx

### Framework support

To support a specific framework, Snyk Code needs to both support the relevant language, and to be trained on projects using the framework. The found patterns are then annotated by our security team and extended by curated content.

Most framework are supported "out of the box" as Snyk Code only need to be able to parse the code to analyze it. In some cases they might require specific rules, or it might require specific program analysis engine update or both. If you notice any gaps in a specific framework support [contact our Support team](https://support.snyk.io/hc/en-us/requests/new) with the details/examples and our team will work on it.

### JavaScript frameworks

{% hint style="info" %}
These are some of the explicitly supported frameworks for JavaScript; those are in addition to the general support for many frameworks.
{% endhint %}

* **React**: Open-source, front end, JavaScript library for building user interfaces or UI components for websites and mobile applications.
* **Vue.js**: Open-source model–view–viewmodel front end JavaScript framework for building user interfaces and single-page applications.
* **Express**: Back-end web application framework for Node.js, released as free and open-source software. It has been called the de facto standard server framework for Node.js.
* **jQuery:** A fast, small, and feature-rich JavaScript library. It makes things like HTML document traversal and manipulation, event handling, animation, ...

### Java frameworks

{% hint style="info" %}
These are some of the explicitly supported frameworks for Java; those are in addition to the general support for many frameworks.
{% endhint %}

* **Apache Camel**: Open source framework for message-oriented middleware with a rule-based routing and mediation engine.
* **Apache Struts**: Open-source, MVC framework for creating elegant, modern Java web applications.
* **Spring MVC**: The Spring Web model-view-controller (MVC) framework.
* **Spring JDBC**: The Spring JDBC data access layer, a simple ORM.
* **Jakarta XML Services**: Framework to implement XML-based Web Services.
* **Dropwizard**: Used for the development of RESTful web services.

### Python frameworks

{% hint style="info" %}
These are some of the explicitly supported frameworks for Python; those are in addition to the general support for many frameworks.
{% endhint %}

* [Django](https://www.djangoproject.com): a framework for full-stack web application development and server development.
* [Flask](https://palletsprojects.com/p/flask/) a lightweight [WSGI](https://wsgi.readthedocs.io) web application framework

### C and C++ frameworks

{% hint style="info" %}
These are some of the explicitly supported frameworks for C/C++; those are in addition to the general support for many frameworks.
{% endhint %}

* C++ Standard Library - a collection of classes and functions from the C++ core language.
* POSIX - a C library for standard POSIX systems.&#x20;
* [Win32](https://win32-framework.sourceforge.net/) - a C++ library used to build windows applications.

### C# frameworks

{% hint style="info" %}
These are some of the explicitly supported frameworks for C#; those are in addition to the general support for many frameworks.
{% endhint %}

* **.NET framework**: .NET is an open source developer platform, created by Microsoft and used to build a variety of application types. Snyk Code supports .NET 6.
* **ASP.NET (version 6.x)**: ASP.NET is a free and open source framework to build web apps and services using .NET. Snyk Code supports version 6.x.
* **.NET Core**: Microsoft created .NET Core to make the .NET framework cross-platform and enable a number of scenarios. The .NET framework and .NET Core share many components and code can be exchanged. (Microsoft [provides guidance](https://docs.microsoft.com/en-us/dotnet/standard/choosing-core-framework-server) when to choose which)

{% hint style="info" %}
The framework support is always determined by the file extensions known to the engine. For example, the engine does not scan **`*.cshtml`** files, but scans the associated **`*.cshtml.cs`** files.
{% endhint %}

### Ruby frameworks

{% hint style="info" %}
These are some of the explicitly supported frameworks for Ruby; those are in addition to the general support for many frameworks.
{% endhint %}

* **Ruby On Rails**: Server side web application framework.

### PHP frameworks

{% hint style="info" %}
These are some of the explicitly supported frameworks for PHP; those are in addition to the general support for many frameworks.
{% endhint %}

* **Symfony**: Backend framework used to build complex applications.
* **Laravel**: Backend framework used to build modern web applications.

### File size limit for Snyk Code analysis

Snyk Code automatically excludes the following files from analysis:

* On the Web UI - files that are larger than 1MB.
* On the CLI and IDE - files that are larger than 1MB.
* Minified JS files with 3 or less lines.

### Filename length limitation

The analysis is available only for files with names shorter or equal to 255 characters. You receive an error if the filename exceeds this limit. To make sure that all files are being analyzed, consider shortening long filenames.
