# Basic Launch EC2 Instance Guide

This file contains a simplified guide for launching AWS EC2 instances with step-by-step screenshots.

## Overview

The guide follows a streamlined approach for launching EC2 instances, focusing on essential configuration steps with practical examples.

## Launch EC2 Instance Flow Diagram

```mermaid
flowchart TD
    A[Start: AWS Console Login] -----> B[Launch Instance from Console]
    B -----> C[Add Name and Tags<br/>Example Server]
    C -----> D[Select Ubuntu AMI]
    D -----> E[Select Instance Type<br/>t2.micro]
    E -----> F[Create Key Pair<br/>Downloads to Machine]
    F -----> G[Configure Network Settings<br/>Create Security Group<br/>SSH Traffic from Anywhere]
    G -----> H[Launch Instance]
    
    %% Image placeholders - add actual dimensions when screenshots are available
    B@{ img: "https://raw.githubusercontent.com/saikiran-private/aws-with-images/main/Class3-EC2/images/launch-console.png", h: 400, w: 800, pos: "t"}
    C@{ img: "https://raw.githubusercontent.com/saikiran-private/aws-with-images/main/Class3-EC2/images/name-tags.png", h: 400, w: 800, pos: "t"}
    D@{ img: "https://raw.githubusercontent.com/saikiran-private/aws-with-images/main/Class3-EC2/images/ubuntu-ami.png", h: 400, w: 800, pos: "t"}
    E@{ img: "https://raw.githubusercontent.com/saikiran-private/aws-with-images/main/Class3-EC2/images/t2-micro-selection.png", h: 400, w: 800, pos: "t"}
    F@{ img: "https://raw.githubusercontent.com/saikiran-private/aws-with-images/main/Class3-EC2/images/keypair-creation.png", h: 400, w: 800, pos: "t"}
    G@{ img: "https://raw.githubusercontent.com/saikiran-private/aws-with-images/main/Class3-EC2/images/security-group-ssh.png", h: 400, w: 800, pos: "t"}
    H@{ img: "https://raw.githubusercontent.com/saikiran-private/aws-with-images/main/Class3-EC2/images/launch-success.png", h: 400, w: 800, pos: "t"}
    
    style A fill:#e1f5fe,font-size:30px
    style B fill:#c8e6c9,font-size:30px
    style C fill:#c8e6c9,font-size:30px
    style D fill:#c8e6c9,font-size:30px
    style E fill:#c8e6c9,font-size:30px
    style F fill:#c8e6c9,font-size:30px
    style G fill:#c8e6c9,font-size:30px
    style H fill:#c8e6c9,font-size:30px
    
    %% Arrow styling - thick arrows
    linkStyle default stroke-width:10px
    linkStyle 0 stroke-width:10px
    linkStyle 1 stroke-width:10px
    linkStyle 2 stroke-width:10px
    linkStyle 3 stroke-width:10px
    linkStyle 4 stroke-width:10px
    linkStyle 5 stroke-width:10px
    linkStyle 6 stroke-width:10px
```

## Basic Process Flow

1. **AWS Console Login** - Access your AWS account 📝
2. **Launch Instance** - Click "Launch Instance" from EC2 console 🔑 ⚠️
3. **Name and Tags** - Add "Example Server" as instance name 🔑 ⚠️
4. **Select Ubuntu AMI** - Choose Ubuntu operating system 🔑 ⚠️
5. **Choose Instance Type** - Select **t2.micro** for free tier 🔑 ⚠️
6. **Create Key Pair** - Generate new key pair, downloads automatically as **.pem** file 🔑 ⚠️
7. **Configure Security Group** - Create new security group with SSH traffic from anywhere 🔑 ⚠️
8. **Launch Instance** - Final launch confirmation 🔑 ⚠️

## Prerequisites

- AWS account with EC2 permissions
- Basic understanding of cloud computing
- SSH client for future connection 
