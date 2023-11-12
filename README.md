# OpenTofu

OpenTofu is an innovative Infrastructure as Code (IaC) tool, designed as a direct replacement for Terraform. It enables developers and infrastructure engineers to define and manage a wide range of resources across multiple providers and services using a simple, declarative syntax.

## Features

- **Multi-Provider Support:** Compatible with a vast array of providers, allowing for management of diverse infrastructure resources.
- **Declarative Syntax:** Utilizes HCL (HashiCorp Configuration Language), offering a human-readable way to describe infrastructure.
- **Seamless Migration:** Designed for backward compatibility with Terraform, making migrations smoother.

## Getting Started

### Prerequisites

- Ensure you have a compatible operating system (Linux, MacOS, Windows).
- Basic understanding of infrastructure management and IaC principles.

### Installation

Download the latest version of OpenTofu from the [releases page](https://github.com/opentofu/opentofu/releases).

#### MacOS Example:

```
bash
wget https://github.com/opentofu/opentofu/releases/download/v1.6.0-alpha2/tofu_1.6.0-alpha2_darwin_arm64.zip
unzip tofu_1.6.0-alpha2_darwin_arm64.zip
mv tofu /usr/local/bin/tofu
```

## Usage

1. Writing Configurations: Define your infrastructure in HCL. Save the configurations in .tf files.

```
provider "aws" {
  region = "us-west-2"
}

resource "aws_instance" "example" {
  ami           = "ami-0c55b159cbfafe1f0"
  instance_type = "t2.micro"
}
```
2. Planning: Generate an execution plan with tofu plan to preview changes.
   
3.Applying Changes: Apply your configuration with tofu apply.
