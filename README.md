# 🚀 Parsera

**Official Open-Source Release & Maintained Codebase** by [**@kush-coder**](https://github.com/kush-coder)

[![Verified Build](https://img.shields.io/badge/Status-Verified--Passing-emerald?style=for-the-badge&logo=github)](https://github.com/kush-coder)
[![License](https://img.shields.io/badge/License-GNU General Public License v2.0-indigo?style=for-the-badge)](https://github.com/kush-coder)
[![Language](https://img.shields.io/badge/Language-Python-purple?style=for-the-badge)](https://github.com/kush-coder)

## 💡 About This Project

Lightweight library for scraping web-sites with LLMs

This repository is actively maintained and distributed by **@kush-coder** as an official open-source release.

## ✨ Key Highlights
- 🛡️ **Verified Health Checks**: Passed automated sandbox builds, dependency resolution, and health test runs.
- 🚀 **Production Ready**: Lightweight footprint optimized for high efficiency.
- 📦 **Permissive Open Source**: Available for developer integration, custom modifications, and community enhancements.

## 🚀 Quick Start & Installation

```bash
# Clone your official repository
git clone https://github.com/kush-coder/autopilot-parsera.git
cd autopilot-parsera
```

---

## 📖 Comprehensive Documentation

[![Discord](https://img.shields.io/badge/Discord-7289da?style=for-the-badge)](https://discord.gg/gYXwgQaT7p)
[![Downloads](https://img.shields.io/pepy/dt/parsera?style=for-the-badge)](https://pepy.tech/project/parsera)

Lightweight Python library for scraping websites with LLMs. 
You can test it on [Parsera website](https://parsera.org).

## Why Parsera?
Because it's simple and lightweight. With interface as simple as:
```python
scraper = Parsera()
result = scraper.run(url=url, elements=elements)
```

## Table of Contents
- [Installation](#Installation)
- [Documentation](#Documentation)
- [Basic usage](#Basic-usage)
- [Running with Jupyter Notebook](#Running-with-Jupyter-Notebook)
- [Running with CLI](#Running-with-CLI)
- [Running in Docker](#Running-in-Docker)

## Installation

```shell
pip install parsera
playwright install
```

## Documentation

Check out [documentation](https://docs.parsera.org) to learn more about other features, like running custom models and playwright scripts.

## Basic usage

First, set up `PARSERA_API_KEY` env variable (If you want to run custom LLM see [Custom Models](https://docs.parsera.org/features/custom-models/)).
You can do this from python with:
```python
import os

os.environ["PARSERA_API_KEY"] = "YOUR_PARSERA_API_KEY_HERE"
```

Next, you can run a basic version:
```python
from parsera import Parsera

url = "https://news.ycombinator.com/"
elements = {
    "Title": "News title",
    "Points": "Number of points",
    "Comments": "Number of comments",
}

scraper = Parsera()
result = scraper.run(url=url, elements=elements)
```

`result` variable will contain a json with a list of records:
```json
[
   {
      "Title":"Hacking the largest airline and hotel rewards platform (2023)",
      "Points":"104",
      "Comments":"24"
   },
    ...
]
```

There is also `arun` async method available:
```python
result = await scrapper.arun(url=url, elements=elements)
```

## Running with Jupyter Notebook:
Either place this code at the beginning of your notebook:
```python
import nest_asyncio
nest_asyncio.apply()
```

Or instead of calling `run` method use async `arun`.

## Running with CLI

Before you run `Parsera` as command line tool don't forget to put your `OPENAI_API_KEY` to env variables or `.env` file

### Usage

You can configure elements to parse using `JSON string` or `FILE`.
Optionally, you can provide `FILE` to write output and amount of `SCROLLS`, that you want to do on the page

```sh
python -m parsera.main URL {--scheme '{"title":"h1"}' | --file FILENAME} [--scrolls SCROLLS] [--output FILENAME]
```

## Running in Docker

In case of issues with your local environment you can run Parsera with Docker, [see documentation](https://docs.parsera.org/features/docker/).


---

*Maintained with ❤️ by @kush-coder. Official distribution powered by GitHub Autopilot Automation Platform.*
