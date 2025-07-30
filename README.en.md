# Xget

**[汉语](README.md)**

[![Chromium Extension](https://img.shields.io/badge/Chromium%20Extension-4285F4?logo=googlechrome&logoColor=white)](#-ecosystem-integration)
[![Cloudflare Workers](https://img.shields.io/badge/Cloudflare%20Workers-F38020?&logo=cloudflare&logoColor=white)](#cloudflare-workers-one-click-deployment)

[![GitHub](https://img.shields.io/badge/GitHub-181717?&logo=github&logoColor=white)](#github)
[![GitLab](https://img.shields.io/badge/GitLab-FC6D26?&logo=gitlab&logoColor=white)](#gitlab)
[![Gitea](https://img.shields.io/badge/Gitea-609926?&logo=gitea&logoColor=white)](#gitea)
[![Codeberg](https://img.shields.io/badge/Codeberg-2185D0?&logo=codeberg&logoColor=white)](#codeberg)
[![SourceForge](https://img.shields.io/badge/SourceForge-FF6600?&logo=sourceforge&logoColor=white)](#sourceforge)
[![Hugging Face](https://img.shields.io/badge/Hugging%20Face-FFD21E?&logo=huggingface&logoColor=white)](#as-hugging-face-mirror)
[![npm](https://img.shields.io/badge/npm-CB3837?logo=npm&logoColor=white)](#npm-package-acceleration)
[![PyPI](https://img.shields.io/badge/PyPI-3775A9?logo=pypi&logoColor=white)](#python-package-acceleration)
[![conda](https://img.shields.io/badge/conda-44A833?logo=anaconda&logoColor=white)](#conda-package-acceleration)
[![Maven](https://img.shields.io/badge/Maven-C71A36?logo=apachemaven&logoColor=white)](#maven-package-acceleration)
[![Gradle](https://img.shields.io/badge/Gradle-02303A?logo=gradle&logoColor=white)](#gradle-package-acceleration)
[![RubyGems](https://img.shields.io/badge/RubyGems-CC342D?logo=rubygems&logoColor=white)](#ruby-package-acceleration)
[![Go](https://img.shields.io/badge/Go-00ADD8?logo=go&logoColor=white)](#go-module-acceleration)
[![NuGet](https://img.shields.io/badge/NuGet-004880?logo=nuget&logoColor=white)](#nuget-package-acceleration)
[![Packagist](https://img.shields.io/badge/Packagist-F28D1A?logo=packagist&logoColor=white)](#php-package-acceleration)
[![Debian](https://img.shields.io/badge/Debian-A81D33?logo=debian&logoColor=white)](#linux-distribution-acceleration)
[![Ubuntu](https://img.shields.io/badge/Ubuntu-E95420?logo=ubuntu&logoColor=white)](#linux-distribution-acceleration)
[![Fedora](https://img.shields.io/badge/Fedora-294172?logo=fedora&logoColor=white)](#linux-distribution-acceleration)
[![Rocky Linux](https://img.shields.io/badge/Rocky%20Linux-10B981?logo=rockylinux&logoColor=white)](#linux-distribution-acceleration)
[![Arch Linux](https://img.shields.io/badge/Arch%20Linux-1793D1?logo=archlinux&logoColor=white)](#linux-distribution-acceleration)
[![arXiv](https://img.shields.io/badge/arXiv-B31B1B?logo=arxiv&logoColor=white)](#academic-resource-acceleration)
[![Container Registry](https://img.shields.io/badge/Container%20Registry-%23007EC6.svg?logo=docker&logoColor=white)](#container-registry)

Ultra-high performance, secure all-in-one open source resource acceleration engine. Its performance far exceeds traditional accelerators, providing you with unified and efficient download experience across multiple platforms, covering code repositories, package management, container images, models and datasets, etc.

## 🎯 Quick Start

**Public Instance:** [**`xget.xi-xu.me`**](https://xget.xi-xu.me) - Ready to use, no deployment required!

> **⚡ Experience lightning-fast downloads instantly**: No registration, no configuration required, use directly to experience blazing fast download speeds!

## 🌟 Core Advantages - Why Choose Xget?

### ⚡ Extreme Performance - Breaking Traditional Accelerator Bottlenecks

- **⚡ Millisecond Response**: Cloudflare's global 330+ edge nodes, average response time < 50ms
- **🌐 HTTP/3 Ultra-fast Protocol**: Latest HTTP/3 protocol enabled, 40% reduced connection latency, 30% improved transfer speed
- **📦 Smart Multi-layer Compression**: Triple compression algorithms (gzip, deflate, brotli), 60% improved transfer efficiency
- **🔗 Zero-latency Pre-connection**: Connection warm-up and keep-alive, eliminating handshake overhead for instant response
- **⚡ Parallel Chunked Downloads**: Full HTTP Range request support, multi-threaded download speed multiplied
- **🎯 Smart Route Optimization**: Automatically select optimal transmission paths, avoiding network congestion nodes

### 🌐 Deep Multi-platform Integration

- **One-stop Multi-platform Support**: Unified support for high-speed downloads from code repositories, package managers, container registries, model and dataset hosting platforms
- **Smart Recognition and Conversion**: Automatically recognize platform prefixes and convert to correct URL structure for target platforms
- **Consistent Acceleration Experience**: Enjoy unified and stable ultra-fast download service regardless of file type or source

### 🔒 Enterprise-grade Security Assurance

- **Multi-layer Security Headers**:
  - `Strict-Transport-Security`: Force HTTPS transmission, prevent man-in-the-middle attacks
  - `X-Frame-Options: DENY`: Prevent clickjacking attacks
  - `X-XSS-Protection`: Built-in XSS protection mechanism
  - `Content-Security-Policy`: Strict content security policy
  - `Referrer-Policy`: Control referrer information leakage
- **Request Validation Mechanism**:
  - HTTP method whitelist: Regular requests limited to GET/HEAD, Git operations dynamically allow POST
  - Path length limit: Prevent overly long URL attacks (maximum 2048 characters)
  - Input sanitization: Prevent path traversal and injection attacks
- **Timeout Protection**: 30-second request timeout, prevent resource exhaustion and malicious requests

### 🚀 Modern Architecture and Reliability

- **Smart Retry Mechanism**:
  - Maximum 3 retries with linear delay strategy (1000ms × retry count)
  - Automatic error recovery, improved download success rate
  - Timeout detection and interruption handling
- **Efficient Caching Strategy**:
  - 1800 seconds (30 minutes) default cache duration, significantly reducing origin server pressure
  - Git operations skip cache to ensure real-time performance
  - Edge caching based on Cloudflare Cache API
- **Performance Monitoring System**:
  - Built-in `PerformanceMonitor` class, real-time tracking of request stage timing
  - Detailed performance data via `X-Performance-Metrics` response header
  - Support for cache hit rate statistics and optimization suggestions

### 🎯 Full Git Protocol Compatibility

- **Smart Protocol Detection**:
  - Automatically recognize Git-specific endpoints (`/info/refs`, `/git-upload-pack`, `/git-receive-pack`)
  - Detect Git client User-Agent patterns
  - Support query parameters like `service=git-upload-pack`
- **Complete Operation Support**:
  - `git clone`: Full repository cloning, support shallow cloning and branch specification
  - `git push`: Code pushing and branch management
  - `git pull/fetch`: Incremental updates and remote synchronization
  - `git submodule`: Recursive submodule cloning
- **Protocol Optimization**:
  - Maintain Git-specific request headers and authentication information
  - Smart User-Agent handling (default `git/2.34.1`)
  - Support Git LFS large file transfer

### 📱 Ecosystem Integration

- **Dedicated Browser Extension**: [Xget for Chromium](https://github.com/xixu-me/Xget-for-Chromium) provides seamless experience
  - Automatic link redirection, no manual URL modification needed
  - Support custom Xget instance domain names
  - Multi-platform preference settings and blacklist/whitelist management
  - Local processing ensures privacy security
- **Download Tool Compatibility**: Perfect support for wget, cURL, aria2, IDM and other mainstream download tools
- **CI/CD Integration**: Can be used directly in GitHub Actions, GitLab CI and other environments

## 📖 Link Conversion Rules

Using the public instance [**`xget.xi-xu.me`**](https://xget.xi-xu.me) or your own deployed instance, simply replace the domain and add platform prefix:

### Conversion Format

| Platform | Platform Prefix | Original Link Format | Accelerated Link Format |
|----------|-----------------|---------------------|-------------------------|
| GitHub | `gh` | `https://github.com/...` | `https://xget.xi-xu.me/gh/...` |
| GitLab | `gl` | `https://gitlab.com/...` | `https://xget.xi-xu.me/gl/...` |
| Gitea | `gitea` | `https://gitea.com/...` | `https://xget.xi-xu.me/gitea/...` |
| Codeberg | `codeberg` | `https://codeberg.org/...` | `https://xget.xi-xu.me/codeberg/...` |
| SourceForge | `sf` | `https://sourceforge.net/...` | `https://xget.xi-xu.me/sf/...` |
| Hugging Face | `hf` | `https://huggingface.co/...` | `https://xget.xi-xu.me/hf/...` |
| npm | `npm` | `https://registry.npmjs.org/...` | `https://xget.xi-xu.me/npm/...` |
| PyPI | `pypi` | `https://pypi.org/...` | `https://xget.xi-xu.me/pypi/...` |
| conda | `conda` | `https://repo.anaconda.com/...` and `https://conda.anaconda.org/...` | `https://xget.xi-xu.me/conda/...` and `https://xget.xi-xu.me/conda/community/...` |
| Maven | `maven` | `https://repo1.maven.org/...` | `https://xget.xi-xu.me/maven/...` |
| Gradle | `gradle` | `https://plugins.gradle.org/...` | `https://xget.xi-xu.me/gradle/...` |
| RubyGems | `rubygems` | `https://rubygems.org/...` | `https://xget.xi-xu.me/rubygems/...` |
| Go Modules | `golang` | `https://proxy.golang.org/...` | `https://xget.xi-xu.me/golang/...` |
| NuGet | `nuget` | `https://api.nuget.org/...` | `https://xget.xi-xu.me/nuget/...` |
| Packagist | `packagist` | `https://repo.packagist.org/...` | `https://xget.xi-xu.me/packagist/...` |
| Debian | `debian` | `https://deb.debian.org/...` | `https://xget.xi-xu.me/debian/...` |
| Ubuntu | `ubuntu` | `https://archive.ubuntu.com/...` | `https://xget.xi-xu.me/ubuntu/...` |
| Fedora | `fedora` | `https://dl.fedoraproject.org/...` | `https://xget.xi-xu.me/fedora/...` |
| Rocky Linux | `rocky` | `https://download.rockylinux.org/...` | `https://xget.xi-xu.me/rocky/...` |
| Arch Linux | `arch` | `https://geo.mirror.pkgbuild.com/...` | `https://xget.xi-xu.me/arch/...` |
| arXiv | `arxiv` | `https://arxiv.org/...` | `https://xget.xi-xu.me/arxiv/...` |
| Container Registry | `cr` | See [Container Registry](#container-registry) | See [Container Registry](#container-registry) |

### Platform Conversion Examples

#### GitHub

```url
# Original link
https://github.com/microsoft/vscode/archive/refs/heads/main.zip

# Converted (add gh prefix)
https://xget.xi-xu.me/gh/microsoft/vscode/archive/refs/heads/main.zip
```

#### GitLab

```url
# Original link
https://gitlab.com/gitlab-org/gitlab/-/archive/master/gitlab-master.zip

# Converted (add gl prefix)
https://xget.xi-xu.me/gl/gitlab-org/gitlab/-/archive/master/gitlab-master.zip
```

#### Gitea

```url
# Original link
https://gitea.com/gitea/gitea/archive/main.zip

# Converted (add gitea prefix)
https://xget.xi-xu.me/gitea/gitea/gitea/archive/main.zip
```

#### Codeberg

```url
# Original link
https://codeberg.org/forgejo/forgejo/archive/forgejo.zip

# Converted (add codeberg prefix)
https://xget.xi-xu.me/codeberg/forgejo/forgejo/archive/forgejo.zip
```

#### SourceForge

```url
# Original link
https://sourceforge.net/projects/sevenzip/files/7-Zip/23.01/7z2301-x64.exe/download

# Converted (add sf prefix)
https://xget.xi-xu.me/sf/projects/sevenzip/files/7-Zip/23.01/7z2301-x64.exe/download
```

#### Hugging Face

```url
# Model file original link
https://huggingface.co/microsoft/DialoGPT-medium/resolve/main/pytorch_model.bin

# Converted (add hf prefix)
https://xget.xi-xu.me/hf/microsoft/DialoGPT-medium/resolve/main/pytorch_model.bin

# Dataset file original link
https://huggingface.co/datasets/rajpurkar/squad/resolve/main/plain_text/train-00000-of-00001.parquet

# Converted (add hf prefix)
https://xget.xi-xu.me/hf/datasets/rajpurkar/squad/resolve/main/plain_text/train-00000-of-00001.parquet
```

#### npm

```url
# Package file original link
https://registry.npmjs.org/react/-/react-18.2.0.tgz

# Converted (add npm prefix)
https://xget.xi-xu.me/npm/react/-/react-18.2.0.tgz

# Package metadata original link
https://registry.npmjs.org/lodash

# Converted (add npm prefix)
https://xget.xi-xu.me/npm/lodash
```

#### PyPI

```url
# Python package file original link
https://pypi.org/packages/source/r/requests/requests-2.31.0.tar.gz

# Converted (add pypi prefix)
https://xget.xi-xu.me/pypi/packages/source/r/requests/requests-2.31.0.tar.gz

# Wheel file original link
https://pypi.org/packages/py3/r/requests/requests-2.31.0-py3-none-any.whl

# Converted (add pypi prefix)
https://xget.xi-xu.me/pypi/packages/py3/r/requests/requests-2.31.0-py3-none-any.whl
```

#### conda

```url
# Default channel package file original link
https://repo.anaconda.com/pkgs/main/linux-64/numpy-1.24.3-py311h08b1b3b_1.conda

# Converted (add conda prefix)
https://xget.xi-xu.me/conda/pkgs/main/linux-64/numpy-1.24.3-py311h08b1b3b_1.conda

# Community channel metadata original link
https://conda.anaconda.org/conda-forge/linux-64/repodata.json

# Converted (add conda/community prefix)
https://xget.xi-xu.me/conda/community/conda-forge/linux-64/repodata.json
```

#### Maven

```url
# Maven Central Repository JAR file original link
https://repo1.maven.org/maven2/org/springframework/spring-core/5.3.21/spring-core-5.3.21.jar

# Converted (add maven prefix)
https://xget.xi-xu.me/maven/maven2/org/springframework/spring-core/5.3.21/spring-core-5.3.21.jar

# Maven metadata original link
https://repo1.maven.org/maven2/org/apache/commons/commons-lang3/maven-metadata.xml

# Converted (add maven prefix)
https://xget.xi-xu.me/maven/maven2/org/apache/commons/commons-lang3/maven-metadata.xml
```

#### Gradle

```url
# Gradle Plugin Portal JAR file original link
https://plugins.gradle.org/m2/org/gradle/gradle-enterprise-gradle-plugin/3.13.4/gradle-enterprise-gradle-plugin-3.13.4.jar

# Converted (add gradle prefix)
https://xget.xi-xu.me/gradle/m2/org/gradle/gradle-enterprise-gradle-plugin/3.13.4/gradle-enterprise-gradle-plugin-3.13.4.jar

# Gradle plugin metadata original link
https://plugins.gradle.org/api/gradle/7.6/plugin/use/org.springframework.boot

# Converted (add gradle prefix)
https://xget.xi-xu.me/gradle/api/gradle/7.6/plugin/use/org.springframework.boot
```

#### RubyGems

```url
# RubyGems package file original link
https://rubygems.org/gems/rails-7.0.4.gem

# Converted (add rubygems prefix)
https://xget.xi-xu.me/rubygems/gems/rails-7.0.4.gem

# RubyGems API original link
https://rubygems.org/api/v1/gems/nokogiri.json

# Converted (add rubygems prefix)
https://xget.xi-xu.me/rubygems/api/v1/gems/nokogiri.json
```

#### Go Modules

```url
# Go module proxy original link
https://proxy.golang.org/github.com/gin-gonic/gin/@v/v1.9.1.zip

# Converted (add golang prefix)
https://xget.xi-xu.me/golang/github.com/gin-gonic/gin/@v/v1.9.1.zip

# Go module info original link
https://proxy.golang.org/github.com/gorilla/mux/@v/list

# Converted (add golang prefix)
https://xget.xi-xu.me/golang/github.com/gorilla/mux/@v/list
```

#### NuGet

```url
# NuGet package download original link
https://api.nuget.org/v3-flatcontainer/newtonsoft.json/13.0.3/newtonsoft.json.13.0.3.nupkg

# Converted (add nuget prefix)
https://xget.xi-xu.me/nuget/v3-flatcontainer/newtonsoft.json/13.0.3/newtonsoft.json.13.0.3.nupkg

# NuGet package metadata original link
https://api.nuget.org/v3/registration5-semver1/microsoft.aspnetcore.app/index.json

# Converted (add nuget prefix)
https://xget.xi-xu.me/nuget/v3/registration5-semver1/microsoft.aspnetcore.app/index.json
```

#### Packagist

```url
# Packagist package metadata original link
https://repo.packagist.org/p2/symfony/console.json

# Converted (add packagist prefix)
https://xget.xi-xu.me/packagist/p2/symfony/console.json

# Packagist package list original link
https://repo.packagist.org/packages/list.json

# Converted (add packagist prefix)
https://xget.xi-xu.me/packagist/packages/list.json
```

#### Linux Distributions

```url
# Debian package original link
https://deb.debian.org/debian/pool/main/c/curl/curl_7.88.1-10+deb12u4_amd64.deb

# Converted (add debian prefix)
https://xget.xi-xu.me/debian/debian/pool/main/c/curl/curl_7.88.1-10+deb12u4_amd64.deb

# Ubuntu package original link
https://archive.ubuntu.com/ubuntu/pool/main/g/git/git_2.34.1-1ubuntu1.9_amd64.deb

# Converted (add ubuntu prefix)
https://xget.xi-xu.me/ubuntu/ubuntu/pool/main/g/git/git_2.34.1-1ubuntu1.9_amd64.deb

# Fedora package original link
https://dl.fedoraproject.org/pub/fedora/linux/releases/39/Everything/x86_64/os/Packages/n/nginx-1.24.0-1.fc39.x86_64.rpm

# Converted (add fedora prefix)
https://xget.xi-xu.me/fedora/pub/fedora/linux/releases/39/Everything/x86_64/os/Packages/n/nginx-1.24.0-1.fc39.x86_64.rpm

# Rocky Linux package original link
https://download.rockylinux.org/pub/rocky/9/BaseOS/x86_64/os/Packages/b/bash-5.1.8-6.el9.x86_64.rpm

# Converted (add rocky prefix)
https://xget.xi-xu.me/rocky/pub/rocky/9/BaseOS/x86_64/os/Packages/b/bash-5.1.8-6.el9.x86_64.rpm

# Arch Linux package original link
https://geo.mirror.pkgbuild.com/core/os/x86_64/linux-6.6.10.arch1-1-x86_64.pkg.tar.zst

# Converted (add arch prefix)
https://xget.xi-xu.me/arch/core/os/x86_64/linux-6.6.10.arch1-1-x86_64.pkg.tar.zst
```

#### arXiv

```url
# arXiv paper PDF original link
https://arxiv.org/pdf/2301.07041.pdf

# Converted (add arxiv prefix)
https://xget.xi-xu.me/arxiv/pdf/2301.07041.pdf

# arXiv paper source original link
https://arxiv.org/e-print/2301.07041

# Converted (add arxiv prefix)
https://xget.xi-xu.me/arxiv/e-print/2301.07041
```

#### Container Registry

Xget supports multiple container registries using the `cr/[container-registry-prefix]` format:

| Container Registry | Registry Prefix | Original Link Format | Accelerated Link Format |
|-------------------|-----------------|---------------------|-------------------------|
| Quay.io | `quay` | `https://quay.io/...` | `https://xget.xi-xu.me/cr/quay/...` |
| Google | `gcr` | `https://gcr.io/...` | `https://xget.xi-xu.me/cr/gcr/...` |
| Microsoft | `mcr` | `https://mcr.microsoft.com/...` | `https://xget.xi-xu.me/cr/mcr/...` |
| Amazon ECR | `ecr` | `https://public.ecr.aws/...` | `https://xget.xi-xu.me/cr/ecr/...` |
| GitHub | `ghcr` | `https://ghcr.io/...` | `https://xget.xi-xu.me/cr/ghcr/...` |
| GitLab | `gitlab` | `https://registry.gitlab.com/...` | `https://xget.xi-xu.me/cr/gitlab/...` |
| Red Hat | `redhat` | `https://registry.redhat.io/...` | `https://xget.xi-xu.me/cr/redhat/...` |
| Oracle | `oracle` | `https://container-registry.oracle.com/...` | `https://xget.xi-xu.me/cr/oracle/...` |
| Cloudsmith | `cloudsmith` | `https://docker.cloudsmith.io/...` | `https://xget.xi-xu.me/cr/cloudsmith/...` |
| DigitalOcean | `digitalocean` | `https://registry.digitalocean.com/...` | `https://xget.xi-xu.me/cr/digitalocean/...` |
| VMware | `vmware` | `https://projects.registry.vmware.com/...` | `https://xget.xi-xu.me/cr/vmware/...` |
| Kubernetes | `k8s` | `https://registry.k8s.io/...` | `https://xget.xi-xu.me/cr/k8s/...` |
| Heroku | `heroku` | `https://registry.heroku.com/...` | `https://xget.xi-xu.me/cr/heroku/...` |
| SUSE | `suse` | `https://registry.suse.com/...` | `https://xget.xi-xu.me/cr/suse/...` |
| openSUSE | `opensuse` | `https://registry.opensuse.org/...` | `https://xget.xi-xu.me/cr/opensuse/...` |
| Gitpod | `gitpod` | `https://registry.gitpod.io/...` | `https://xget.xi-xu.me/cr/gitpod/...` |

```url
# GitHub Container Registry original link
https://ghcr.io/v2/nginxinc/nginx-unprivileged/manifests/latest

# Converted (add cr/ghcr prefix)
https://xget.xi-xu.me/cr/ghcr/v2/nginxinc/nginx-unprivileged/manifests/latest

# Google Container Registry original link
https://gcr.io/v2/distroless/base/manifests/latest

# Converted (add cr/gcr prefix)
https://xget.xi-xu.me/cr/gcr/v2/distroless/base/manifests/latest
```

## 🎯 Use Cases

### Git Operations and Configuration

Xget is fully compatible with Git protocol, supports all standard Git operations, and provides global acceleration configuration:

#### Git Operations

```bash
# Clone repository
git clone https://xget.xi-xu.me/gh/microsoft/vscode.git

# Clone specific branch
git clone -b main https://xget.xi-xu.me/gh/facebook/react.git

# Shallow clone (latest commit only)
git clone --depth 1 https://xget.xi-xu.me/gh/torvalds/linux.git

# Clone GitLab repository
git clone https://xget.xi-xu.me/gl/gitlab-org/gitlab.git

# Clone Gitea repository
git clone https://xget.xi-xu.me/gitea/gitea/gitea.git

# Clone Codeberg repository
git clone https://xget.xi-xu.me/codeberg/forgejo/forgejo.git

# Clone SourceForge repository
git clone https://xget.xi-xu.me/sf/projects/mingw-w64/code.git

# Add remote repository
git remote add upstream https://xget.xi-xu.me/gh/[owner]/[repository].git

# Pull updates
git pull https://xget.xi-xu.me/gh/microsoft/vscode.git main

# Recursive submodule clone
git clone --recursive https://xget.xi-xu.me/gh/[username]/[repository-with-submodules].git
```

#### Git Global Acceleration Configuration

```bash
# Configure Git to use Xget for specific domains
git config --global url."https://xget.xi-xu.me/gh/".insteadOf "https://github.com/"
git config --global url."https://xget.xi-xu.me/gl/".insteadOf "https://gitlab.com/"
git config --global url."https://xget.xi-xu.me/gitea/".insteadOf "https://gitea.com/"
git config --global url."https://xget.xi-xu.me/codeberg/".insteadOf "https://codeberg.org/"
git config --global url."https://xget.xi-xu.me/sf/".insteadOf "https://sourceforge.net/"

# Verify configuration
git config --global --get-regexp url

# Now all git clone operations for related platforms will automatically use Xget acceleration
git clone https://github.com/microsoft/vscode.git  # Automatically converted to Xget link
git clone https://gitlab.com/gitlab-org/gitlab.git  # Automatically converted to Xget link
git clone https://codeberg.org/forgejo/forgejo.git  # Automatically converted to Xget link
```

### Mainstream Download Tool Integration

#### wget Downloads

```bash
# Download single file
wget https://xget.xi-xu.me/gh/microsoft/vscode/archive/refs/heads/main.zip

# Resume download
wget -c https://xget.xi-xu.me/hf/microsoft/DialoGPT-large/resolve/main/pytorch_model.bin

# Batch download
wget -i urls.txt  # urls.txt contains multiple Xget links
```

#### cURL Downloads

```bash
# Basic download
curl -L -O https://xget.xi-xu.me/gh/golang/go/archive/refs/tags/go1.22.0.tar.gz

# Show progress bar
curl -L --progress-bar -o model.bin https://xget.xi-xu.me/hf/openai/whisper-large-v3/resolve/main/pytorch_model.bin

# Set user agent
curl -L -H "User-Agent: MyApp/1.0" https://xget.xi-xu.me/gl/gitlab-org/gitlab-runner/-/archive/main/gitlab-runner-main.zip
```

#### aria2 Multi-threaded Downloads

```bash
# Multi-threaded download for large files
aria2c -x 16 -s 16 https://xget.xi-xu.me/hf/microsoft/DialoGPT-large/resolve/main/pytorch_model.bin

# Resume download
aria2c -c https://xget.xi-xu.me/gh/microsoft/vscode/archive/refs/heads/main.zip

# Batch download with config file
aria2c -i download-list.txt  # File containing multiple Xget links
```

### As Hugging Face Mirror

```python
import os
from transformers import AutoTokenizer, AutoModelForCausalLM

# Set environment variable to make transformers library automatically use Xget mirror
os.environ['HF_ENDPOINT'] = 'https://xget.xi-xu.me/hf'

# Define model name
model_name = 'microsoft/DialoGPT-medium'

print(f"Downloading model from mirror: {model_name}")

# Use AutoModelForCausalLM to load conversational generation model
# No additional parameters needed due to environment variable set above
tokenizer = AutoTokenizer.from_pretrained(model_name)
model = AutoModelForCausalLM.from_pretrained(model_name)

print("Model and tokenizer loaded successfully!")

# You can now use the tokenizer and model
# For example:
# new_user_input_ids = tokenizer.encode("Hello, how are you?", return_tensors='pt')
# chat_history_ids = model.generate(new_user_input_ids, max_length=1000, pad_token_id=tokenizer.eos_token_id)
# print(tokenizer.decode(chat_history_ids[:, new_user_input_ids.shape[-1]:][0], skip_special_tokens=True))
```

### npm Package Acceleration

#### Configure npm to use Xget mirror

```bash
# Temporarily use Xget mirror
npm install --registry https://xget.xi-xu.me/npm/

# Globally configure npm mirror
npm config set registry https://xget.xi-xu.me/npm/

# Verify configuration
npm config get registry
```

#### Use in projects

```bash
# Configure project-level mirror in .npmrc file
echo "registry=https://xget.xi-xu.me/npm/" > .npmrc

# Install dependencies
npm install

# Or use yarn
yarn config set registry https://xget.xi-xu.me/npm/
yarn install
```

### Python Package Acceleration

#### Configure pip to use Xget mirror

```bash
# Temporarily use Xget mirror
pip install requests -i https://xget.xi-xu.me/pypi/simple/

# Globally configure pip mirror
pip config set global.index-url https://xget.xi-xu.me/pypi/simple/
pip config set global.trusted-host xget.xi-xu.me

# Verify configuration
pip config list
```

#### Use in projects

```bash
# Create pip.conf file (Linux/macOS)
mkdir -p ~/.pip
cat > ~/.pip/pip.conf << EOF
[global]
index-url = https://xget.xi-xu.me/pypi/simple/
trusted-host = xget.xi-xu.me
EOF

# Or create pip.conf in project root directory
cat > pip.conf << EOF
[global]
index-url = https://xget.xi-xu.me/pypi/simple/
trusted-host = xget.xi-xu.me
EOF

# Install using config file
pip install -r requirements.txt --config-file pip.conf
```

#### Specify mirror in requirements.txt

```txt
# requirements.txt
--index-url https://xget.xi-xu.me/pypi/simple/
--trusted-host xget.xi-xu.me

requests>=2.25.0
numpy>=1.21.0
pandas>=1.3.0
matplotlib>=3.4.0
```

### conda Package Acceleration

#### Configure conda to use Xget mirror

```bash
# Configure default channel mirrors
conda config --add default_channels https://xget.xi-xu.me/conda/pkgs/msys2
conda config --add default_channels https://xget.xi-xu.me/conda/pkgs/r
conda config --add default_channels https://xget.xi-xu.me/conda/pkgs/main

# Configure all community channel mirrors (recommended)
conda config --set channel_alias https://xget.xi-xu.me/conda/community

# Or configure specific community channels
conda config --add channels https://xget.xi-xu.me/conda/community/conda-forge
conda config --add channels https://xget.xi-xu.me/conda/community/bioconda

# Set channel priority
conda config --set channel_priority strict

# Verify configuration
conda config --show
```

#### Configure in .condarc

The .condarc file can be placed in the user home directory (`~/.condarc`) or project root directory:

```yaml
default_channels:
  - https://xget.xi-xu.me/conda/pkgs/main
  - https://xget.xi-xu.me/conda/pkgs/r
  - https://xget.xi-xu.me/conda/pkgs/msys2
channel_alias: https://xget.xi-xu.me/conda/community
channel_priority: strict
show_channel_urls: true
```

#### Use environment files

Environment files can directly specify complete mirror URLs:

```yaml
# environment.yml
name: myproject
channels:
  - https://xget.xi-xu.me/conda/pkgs/main
  - https://xget.xi-xu.me/conda/pkgs/r
  - https://xget.xi-xu.me/conda/community/bioconda
  - https://xget.xi-xu.me/conda/community/conda-forge
dependencies:
  - python=3.11
  - numpy>=1.24.0
  - pandas>=2.0.0
  - matplotlib>=3.7.0
  - scipy>=1.10.0
  - pip
  - pip:
    - requests>=2.28.0
```

```bash
# Create environment using environment file
conda env create -f environment.yml

# Update environment
conda env update -f environment.yml
```

### Maven Package Acceleration

#### Configure Maven to use Xget mirror

```xml
<!-- Configure Maven mirror in ~/.m2/settings.xml -->
<settings>
  <mirrors>
    <mirror>
      <id>xget-maven-central</id>
      <mirrorOf>central</mirrorOf>
      <name>Xget Maven Central Mirror</name>
      <url>https://xget.xi-xu.me/maven/maven2</url>
    </mirror>
  </mirrors>
</settings>
```

#### Use in projects

```xml
<!-- Configure project-level mirror in pom.xml -->
<project>
  <repositories>
    <repository>
      <id>xget-maven-central</id>
      <name>Xget Maven Central</name>
      <url>https://xget.xi-xu.me/maven/maven2</url>
    </repository>
  </repositories>
  
  <pluginRepositories>
    <pluginRepository>
      <id>xget-maven-central</id>
      <name>Xget Maven Central</name>
      <url>https://xget.xi-xu.me/maven/maven2</url>
    </pluginRepository>
  </pluginRepositories>
</project>
```

```bash
# Use command line to specify mirror
mvn clean install -Dmaven.repo.remote=https://xget.xi-xu.me/maven/maven2

# Download specific dependency
mvn dependency:get -Dartifact=org.springframework:spring-core:5.3.21 \
  -DremoteRepositories=https://xget.xi-xu.me/maven/maven2
```

### Gradle Package Acceleration

#### Configure Gradle to use Xget mirror

```gradle
// Configure Gradle mirror in build.gradle
repositories {
    maven {
        url 'https://xget.xi-xu.me/maven/maven2'
    }
    gradlePluginPortal {
        url 'https://xget.xi-xu.me/gradle/m2'
    }
}

// Configure plugin repositories
pluginManagement {
    repositories {
        maven {
            url 'https://xget.xi-xu.me/gradle/m2'
        }
        gradlePluginPortal()
    }
}
```

#### Global configuration

```gradle
// Configure global mirror in ~/.gradle/init.gradle
allprojects {
    repositories {
        maven {
            url 'https://xget.xi-xu.me/maven/maven2'
        }
    }
}

settingsEvaluated { settings ->
    settings.pluginManagement {
        repositories {
            maven {
                url 'https://xget.xi-xu.me/gradle/m2'
            }
            gradlePluginPortal()
        }
    }
}
```

```bash
# Use command line to specify mirror
gradle build -Dmaven.repo.remote=https://xget.xi-xu.me/maven/maven2

# Refresh dependencies
gradle build --refresh-dependencies
```

### Ruby Package Acceleration

#### Configure RubyGems to use Xget mirror

```bash
# Temporarily use Xget mirror
gem install rails --source https://xget.xi-xu.me/rubygems/

# Globally configure RubyGems mirror
gem sources --add https://xget.xi-xu.me/rubygems/
gem sources --remove https://rubygems.org/

# Verify configuration
gem sources -l
```

#### Use in projects

```ruby
# Configure project-level mirror in Gemfile
source 'https://xget.xi-xu.me/rubygems/'

gem 'rails', '~> 7.0.0'
gem 'pg', '~> 1.1'
gem 'puma', '~> 5.0'
```

```bash
# Use bundle to install
bundle config mirror.https://rubygems.org https://xget.xi-xu.me/rubygems/
bundle install
```

### Go Module Acceleration

#### Configure Go to use Xget proxy

```bash
# Configure Go module proxy
export GOPROXY=https://xget.xi-xu.me/golang,direct
export GOSUMDB=off

# Or configure permanently
go env -w GOPROXY=https://xget.xi-xu.me/golang,direct
go env -w GOSUMDB=off

# Verify configuration
go env GOPROXY
```

#### Use in projects

```bash
# Download dependencies
go mod download

# Update dependencies
go get -u ./...

# Clean module cache
go clean -modcache
```

### NuGet Package Acceleration

#### Configure NuGet to use Xget mirror

```bash
# Add Xget package source
dotnet nuget add source https://xget.xi-xu.me/nuget/v3/index.json -n xget

# List package sources
dotnet nuget list source

# Use in project
dotnet restore --source https://xget.xi-xu.me/nuget/v3/index.json
```

#### Configure in NuGet.Config

```xml
<!-- NuGet.Config -->
<?xml version="1.0" encoding="utf-8"?>
<configuration>
  <packageSources>
    <add key="xget" value="https://xget.xi-xu.me/nuget/v3/index.json" />
  </packageSources>
</configuration>
```

### PHP Package Acceleration

#### Configure Composer to use Xget mirror

```bash
# Globally configure Composer mirror
composer config -g repo.packagist composer https://xget.xi-xu.me/packagist/

# Project-level configuration
composer config repo.packagist composer https://xget.xi-xu.me/packagist/

# Verify configuration
composer config -l
```

#### Configure in composer.json

```json
{
  "repositories": [
    {
      "type": "composer",
      "url": "https://xget.xi-xu.me/packagist/"
    }
  ],
  "require": {
    "symfony/console": "^6.0",
    "guzzlehttp/guzzle": "^7.0"
  }
}
```

### Linux Distribution Acceleration

#### Debian/Ubuntu APT Configuration

```bash
# Backup original sources list
sudo cp /etc/apt/sources.list /etc/apt/sources.list.backup

# Configure Debian mirror
echo "deb https://xget.xi-xu.me/debian/debian bookworm main" | sudo tee /etc/apt/sources.list
echo "deb https://xget.xi-xu.me/debian/debian-security bookworm-security main" | sudo tee -a /etc/apt/sources.list

# Configure Ubuntu mirror
echo "deb https://xget.xi-xu.me/ubuntu/ubuntu jammy main restricted universe multiverse" | sudo tee /etc/apt/sources.list
echo "deb https://xget.xi-xu.me/ubuntu/ubuntu jammy-updates main restricted universe multiverse" | sudo tee -a /etc/apt/sources.list

# Update package list
sudo apt update
```

#### Fedora DNF Configuration

```bash
# Configure Fedora mirror
sudo sed -i 's|^metalink=|#metalink=|g' /etc/yum.repos.d/fedora*.repo
sudo sed -i 's|^#baseurl=http://download.example/pub/fedora/linux|baseurl=https://xget.xi-xu.me/fedora/pub/fedora/linux|g' /etc/yum.repos.d/fedora*.repo

# Update package cache
sudo dnf makecache
```

#### Rocky Linux DNF Configuration

```bash
# Configure Rocky Linux mirror
sudo sed -i 's|^mirrorlist=|#mirrorlist=|g' /etc/yum.repos.d/rocky*.repo
sudo sed -i 's|^#baseurl=http://dl.rockylinux.org|baseurl=https://xget.xi-xu.me/rocky|g' /etc/yum.repos.d/rocky*.repo

# Update package cache
sudo dnf makecache
```

#### Arch Linux Pacman Configuration

```bash
# Backup original mirror list
sudo cp /etc/pacman.d/mirrorlist /etc/pacman.d/mirrorlist.backup

# Configure Arch Linux mirror
echo 'Server = https://xget.xi-xu.me/arch/$repo/os/$arch' | sudo tee /etc/pacman.d/mirrorlist

# Update package database
sudo pacman -Sy
```

### Academic Resource Acceleration

#### arXiv Paper Downloads

```bash
# Download arXiv paper PDF
wget https://xget.xi-xu.me/arxiv/pdf/2301.07041.pdf

# Download paper source
curl -L -O https://xget.xi-xu.me/arxiv/e-print/2301.07041

# Batch download multiple papers
for id in 2301.07041 2302.13971 2303.08774; do
  wget https://xget.xi-xu.me/arxiv/pdf/${id}.pdf
done
```

#### Use in academic tools

```python
# Use arXiv acceleration downloads in Python
import requests

def download_arxiv_paper(arxiv_id, output_path):
    url = f"https://xget.xi-xu.me/arxiv/pdf/{arxiv_id}.pdf"
    response = requests.get(url)
    
    if response.status_code == 200:
        with open(output_path, 'wb') as f:
            f.write(response.content)
        print(f"Downloaded {arxiv_id} to {output_path}")
    else:
        print(f"Failed to download {arxiv_id}")

# Download paper
download_arxiv_paper("2301.07041", "attention_is_all_you_need.pdf")
```

### Container Image Acceleration

Xget provides comprehensive acceleration support for container image pulling, compatible with Docker, Podman, containerd and other container runtimes.

#### Docker Configuration

```bash
# Configure Docker to use Xget image acceleration
# Edit /etc/docker/daemon.json (Linux) or ~/.docker/daemon.json (macOS/Windows)
{
  "registry-mirrors": [
    "https://xget.xi-xu.me/cr/ghcr"
  ]
}

# Restart Docker service
sudo systemctl restart docker  # Linux
# Or restart service in Docker Desktop

# Verify configuration
docker info | grep -A 10 "Registry Mirrors"
```

#### Direct Image Pulling

```bash
# Pull GitHub Container Registry images
docker pull xget.xi-xu.me/cr/ghcr/nginxinc/nginx-unprivileged:latest

# Pull Google Container Registry images
docker pull xget.xi-xu.me/cr/gcr/distroless/base:latest

# Pull Microsoft Container Registry images
docker pull xget.xi-xu.me/cr/mcr/dotnet/runtime:8.0
```

#### Kubernetes Deployment Configuration

```yaml
# deployment.yaml - Using Xget accelerated images
apiVersion: apps/v1
kind: Deployment
metadata:
  name: nginx-deployment
spec:
  replicas: 3
  selector:
    matchLabels:
      app: nginx
  template:
    metadata:
      labels:
        app: nginx
    spec:
      containers:
      - name: nginx
        image: xget.xi-xu.me/cr/ghcr/nginxinc/nginx-unprivileged:latest
        ports:
        - containerPort: 80
      - name: redis
        image: xget.xi-xu.me/cr/ghcr/bitnami/redis:alpine
        ports:
        - containerPort: 6379
```

#### Docker Compose Configuration

```yaml
# docker-compose.yml - Using Xget accelerated images
version: '3.8'
services:
  web:
    image: xget.xi-xu.me/cr/ghcr/nginxinc/nginx-unprivileged:latest
    ports:
      - "80:80"
    volumes:
      - ./html:/usr/share/nginx/html
  
  database:
    image: xget.xi-xu.me/cr/mcr/mssql/server:2022-latest
    environment:
      ACCEPT_EULA: Y
      SA_PASSWORD: "MyStrongPassword123!"
    volumes:
      - mssql_data:/var/opt/mssql
  
  cache:
    image: xget.xi-xu.me/cr/ghcr/bitnami/redis:alpine
    ports:
      - "6379:6379"

volumes:
  mssql_data:
```

#### Dockerfile Optimization

```dockerfile
# Use Xget accelerated base images in Dockerfile
FROM xget.xi-xu.me/cr/ghcr/nodejs/node:18-alpine AS builder

WORKDIR /app
COPY package*.json ./
RUN npm install

COPY . .
RUN npm run build

# Production stage
FROM xget.xi-xu.me/cr/ghcr/nginxinc/nginx-unprivileged:latest
COPY --from=builder /app/dist /usr/share/nginx/html

# Use Microsoft Container Registry .NET images
FROM xget.xi-xu.me/cr/mcr/dotnet/aspnet:8.0 AS runtime
WORKDIR /app
COPY --from=builder /app/publish .
ENTRYPOINT ["dotnet", "MyApp.dll"]
```

#### CI/CD Integration

```yaml
# GitHub Actions - Using Xget accelerated container builds
name: Build and Deploy
on: [push]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      
      - name: Build with accelerated base images
        run: |
          # Build using Xget accelerated base images
          docker build -t myapp:latest \
            --build-arg BASE_IMAGE=xget.xi-xu.me/cr/ghcr/nodejs/node:18-alpine .
          
      - name: Test with accelerated images
        run: |
          # Test using accelerated images
          docker run --rm \
            xget.xi-xu.me/cr/mcr/dotnet/runtime:8.0 \
            dotnet --version
```

#### Podman Configuration

```bash
# Configure Podman to use Xget image acceleration
# Edit /etc/containers/registries.conf
[[registry]]
prefix = "ghcr.io"
location = "xget.xi-xu.me/cr/ghcr"

# Or pull directly
podman pull xget.xi-xu.me/cr/ghcr/alpine/alpine:latest
podman pull xget.xi-xu.me/cr/ghcr/nginxinc/nginx-unprivileged:latest
```

#### containerd Configuration

```toml
# Configure containerd to use Xget acceleration
# Edit /etc/containerd/config.toml
[plugins."io.containerd.grpc.v1.cri".registry.mirrors]
  [plugins."io.containerd.grpc.v1.cri".registry.mirrors."ghcr.io"]
    endpoint = ["https://xget.xi-xu.me/cr/ghcr"]
  [plugins."io.containerd.grpc.v1.cri".registry.mirrors."gcr.io"]
    endpoint = ["https://xget.xi-xu.me/cr/gcr"]
```

```bash
# Restart containerd
sudo systemctl restart containerd
```

### CI/CD Environment Integration

#### GitHub Actions

```yaml
name: Download Dependencies
on: [push]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout code
        uses: actions/checkout@v4
      
      - name: Download model files
        run: |
          # Use Xget acceleration to download large model files
          wget https://xget.xi-xu.me/hf/microsoft/DialoGPT-medium/resolve/main/pytorch_model.bin
          
      - name: Clone dependency repo
        run: |
          # Use Xget acceleration for Git cloning
          git clone https://xget.xi-xu.me/gh/[owner]/[repository].git
          
      - name: Download release assets
        run: |
          # Batch download release files
          curl -L -O https://xget.xi-xu.me/gh/[owner]/[repository]/releases/download/v1.0.0/[filename].tar.gz
          curl -L -O https://xget.xi-xu.me/gh/[owner]/[repository]/releases/download/v1.0.0/[filename].zip
```

#### GitLab CI

```yaml
stages:
  - download
  - build

download_dependencies:
  stage: download
  script:
    # Use Xget acceleration for downloads
    - wget https://xget.xi-xu.me/gl/gitlab-org/gitlab-runner/-/archive/main/gitlab-runner-main.zip
    - git clone https://xget.xi-xu.me/gh/[owner]/[dependency-repository].git
    # Download Hugging Face datasets
    - curl -L -O https://xget.xi-xu.me/hf/datasets/wikitext/resolve/main/wikitext-103-v1/wiki.train.tokens
  artifacts:
    paths:
      - "*.zip"
      - "*.json"
      - dependency/
```

#### Docker Build Optimization

```dockerfile
FROM ubuntu:22.04

# Use Xget acceleration for downloads in Docker builds
RUN apt-get update && apt-get install -y wget curl git

# Download large files
RUN wget https://xget.xi-xu.me/gh/microsoft/vscode/archive/refs/heads/main.zip

# Clone source code
RUN git clone https://xget.xi-xu.me/gh/[owner]/[source-repository].git /app

# Download model files
RUN curl -L -O /models/model.bin https://xget.xi-xu.me/hf/microsoft/DialoGPT-medium/resolve/main/pytorch_model.bin

# Configure and install conda packages
RUN echo "default_channels:" > ~/.condarc && \
    echo "  - https://xget.xi-xu.me/conda/pkgs/main" >> ~/.condarc && \
    echo "  - https://xget.xi-xu.me/conda/pkgs/r" >> ~/.condarc && \
    echo "  - https://xget.xi-xu.me/conda/pkgs/msys2" >> ~/.condarc && \
    echo "channel_alias: https://xget.xi-xu.me/conda/community" >> ~/.condarc && \
    echo "channel_priority: strict" >> ~/.condarc && \
    conda install -y numpy pandas matplotlib

WORKDIR /app
```

## 🚀 Deployment Options

### Cloudflare Workers One-Click Deployment

[![Deploy to Cloudflare Workers](https://deploy.workers.cloudflare.com/button)](https://deploy.workers.cloudflare.com/?url=https://github.com/xixu-me/Xget)

After deployment, your Xget service will be available at `your-worker-name.your-subdomain.workers.dev`.

### Manual Deployment

If you prefer manual deployment or need custom configuration:

#### Prerequisites

1. Register a [Cloudflare account](https://dash.cloudflare.com/sign-up/workers-and-pages)
2. Install [Node.js](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm)

#### Deployment Steps

1. **Clone the repository**

   ```bash
   git clone https://github.com/xixu-me/Xget.git
   cd Xget
   ```

2. **Install dependencies and authenticate**

   ```bash
   npm install
   npx wrangler auth login
   ```

3. **Custom configuration (optional)**

   Edit the `wrangler.toml` file to set your repository name:

   ```toml
   name = "your-xget-project-name"
   ```

4. **Deploy**

   ```bash
   npm run deploy
   ```

After deployment, your Xget service will be available at `your-worker-name.your-subdomain.workers.dev`.

## 🔧 Configuration

### Configuration Parameters

You can customize configuration by modifying `src/config/index.js`:

```javascript
export const CONFIG = {
  TIMEOUT_SECONDS: 30,       // Request timeout (seconds)
  MAX_RETRIES: 3,            // Maximum retry attempts
  RETRY_DELAY_MS: 1000,      // Retry delay (milliseconds)
  CACHE_DURATION: 1800,      // Cache duration (1800 seconds = 30 minutes)
  SECURITY: {
    ALLOWED_METHODS: ["GET", "HEAD"],  // Allowed HTTP methods (Git operations dynamically allow POST)
    ALLOWED_ORIGINS: ["*"],            // Allowed CORS origins
    MAX_PATH_LENGTH: 2048,             // Maximum path length (characters)
  },
};
```

### Performance Tuning Recommendations

- **Cache Optimization**: Adjust `CACHE_DURATION` based on usage patterns, reduce for frequently updated repositories
- **Timeout Settings**: Increase `TIMEOUT_SECONDS` appropriately for poor network conditions
- **Retry Strategy**: Increase `MAX_RETRIES` and `RETRY_DELAY_MS` for high-latency environments

### Adding New Platforms

To add support for new platforms, edit `src/config/platforms.js`:

```javascript
export const PLATFORMS = {
  // Existing platforms...
  
  // New platform example
  custom: {
    base: "https://example.com",
    transform: (path) => path.replace(/^\/custom\//, "/"),
  },
};
```

## 🚧 Development

1. **Repository Setup**

   ```bash
   git clone https://github.com/xixu-me/Xget.git
   cd Xget
   npm install
   npx wrangler auth login  # First time use
   ```

2. **Local Development**

   ```bash
   npm run dev              # Start development server (http://localhost:8787)
   npm run test:run         # Run complete test suite
   npm run test:coverage    # Generate test coverage report
   npm run lint             # Code linting
   npm run format           # Code formatting
   npm run deploy           # Deploy to production
   ```

## 🧪 Testing

The repository includes a complete test suite to ensure code quality and functional correctness.

### Complete Testing

```bash
# Install test dependencies
npm install

# Run all tests
npm run test:run

# Generate coverage report
npm run test:coverage

# Watch mode
npm run test:watch
```

### Test Coverage

- **Unit Tests**: Core functionality, platform configuration, performance monitoring
- **Integration Tests**: End-to-end processes, platform integration, Git protocol
- **Security Tests**: Input validation, security headers, permission control
- **Performance Tests**: Response time, memory usage, concurrent processing

## 🔍 Troubleshooting

### Common Issues

**Q: Download speed not significantly improved?**  
A: Check if source files are already cached on CDN edge nodes. First access may be slower, subsequent access will be significantly improved.

**Q: Git operations failing?**  
A: Confirm correct URL format is used and Git client version supports HTTPS proxy.

**Q: Cannot access after deployment?**  
A: Check if Cloudflare Workers domain is correctly bound, confirm `wrangler.toml` configuration is correct.

**Q: Getting 400 errors?**  
A: Check URL path format, confirm platform prefix is used correctly.

### Performance Monitoring

The service returns performance metrics in response headers:

- `X-Performance-Metrics`: Contains timing statistics for various request stages
- `X-Cache-Status`: Shows cache hit status

### Debug Logging

In development environment, you can view detailed logs through Cloudflare Workers console:

```bash
npx wrangler dev --log-level debug
```

## ⚠️ Disclaimer

- **Legal Use**: This repository is only for accelerating legal public file downloads and Git operations. Please comply with relevant platform terms of service and local laws and regulations
- **Service Availability**: Public instance `xget.xi-xu.me` is a free service with no guarantee of 100% availability. Recommend deploying your own instance for production environments
- **Data Security**: Although Xget does not store or log user data, please handle sensitive information downloads carefully
- **Liability Limitation**: Developers are not responsible for any direct or indirect losses caused by using this service
- **Third-party Platforms**: Please respect the terms of service and rate limits of GitHub, GitLab, Gitea, Codeberg, SourceForge, Hugging Face and other platforms

## 🤝 Contributing

We welcome all forms of contributions! Please check the [Contributing Guide](CONTRIBUTING.md) to learn how to participate in repository development.

1. **Report Issues**: Use [issue templates](https://github.com/xixu-me/Xget/issues/new/choose) to report bugs or request features
2. **Submit Code**: Fork the repository, create feature branches, submit pull requests
3. **Improve Documentation**: Fix errors, add examples, improve descriptions
4. **Test Feedback**: Test in different environments and provide feedback

## 🌟 Star History

<a href="https://www.star-history.com/#xixu-me/Xget&Date">
 <picture>
   <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/svg?repos=xixu-me/Xget&type=Date&theme=dark" />
   <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/svg?repos=xixu-me/Xget&type=Date" />
   <img alt="Star History Chart" src="https://api.star-history.com/svg?repos=xixu-me/Xget&type=Date" />
 </picture>
</a>

## 📞 Contact

- **Author**: [Xi Xu](https://xi-xu.me)
- **Email**: [Contact Email](mailto:i@xi-xu.me)
- **Sponsor**: [Sponsor Link](https://xi-xu.me/#sponsorships)

## 📝 License

This repository is licensed under the GPL-3.0 License - see the [LICENSE](LICENSE) file for details.

---

<div align="center">

**If this repository helps you, please consider giving it a ⭐ star!**

Made with ❤️ by [Xi Xu](https://xi-xu.me)

</div>
