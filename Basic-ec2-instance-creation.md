# Basic EC2 Instance Creation Guide

This file contains a simplified guide for creating AWS EC2 instances using default settings with step-by-step screenshots.

## Overview

The guide follows a streamlined approach for basic EC2 instance creation, focusing on essential steps with default configurations. Screenshots focus on core concepts that remain stable despite UI changes.

## EC2 Creation Flow Diagram

```mermaid
flowchart TD
    A[Start: AWS Console Login] -----> B[Navigate to EC2 Dashboard]
    B -----> C[Click Launch Instance]
    C -----> D[Choose AMI]
    D -----> E[Choose Instance Type]
    E -----> F[Configure Instance<br/>Use Default Settings]
    F -----> G[Add Storage<br/>Use Default Settings]
    G -----> H[Configure Security Group]
    H -----> I[Review and Launch]
    I -----> J[Create Key Pair]
    J -----> K[Download Key Pair]
    K -----> L[Instance Running]
    L -----> M[Connect to Instance]
    
    D@{ img: "https://raw.githubusercontent.com/saikiran-private/aws-with-images/main/images/ami-selection.png", h: 430, w: 1270, pos: "t"}
    E@{ img: "https://raw.githubusercontent.com/saikiran-private/aws-with-images/main/images/instance-type.png", h: 446, w: 1544, pos: "t"}
    H@{ img: "https://raw.githubusercontent.com/saikiran-private/aws-with-images/main/images/security-group.png", h: 892, w: 1490, pos: "t"}
    J@{ img: "https://raw.githubusercontent.com/saikiran-private/aws-with-images/main/images/create-keypair.png", h: 510, w: 1646, pos: "t"}
    K@{ img: "https://raw.githubusercontent.com/saikiran-private/aws-with-images/main/images/download-keypair.png", h: 1198, w: 1240, pos: "t"}
    L@{ img: "https://raw.githubusercontent.com/saikiran-private/aws-with-images/main/images/running-instance.png", h: 602, w: 2748, pos: "t"}
    
    style A fill:#e1f5fe,font-size:30px
    style L fill:#c8e6c9,font-size:30px
    style M fill:#c8e6c9,font-size:30px
    style D fill:#c8e6c9,font-size:30px
    style E fill:#c8e6c9,font-size:30px
    style H fill:#c8e6c9,font-size:30px
    style J fill:#c8e6c9,font-size:30px
    style K fill:#c8e6c9,font-size:30px
    style B font-size:30px
    style C font-size:30px
    style F font-size:30px
    style G font-size:30px
    style I font-size:30px
    
    %% Arrow styling - thick arrows
    linkStyle default stroke-width:10px
    linkStyle 0 stroke-width:10px
    linkStyle 1 stroke-width:10px
    linkStyle 2 stroke-width:10px
    linkStyle 3 stroke-width:10px
    linkStyle 4 stroke-width:10px
    linkStyle 5 stroke-width:10px
    linkStyle 6 stroke-width:10px
    linkStyle 7 stroke-width:10px
    linkStyle 8 stroke-width:10px
    linkStyle 9 stroke-width:10px
    linkStyle 10 stroke-width:10px
    linkStyle 11 stroke-width:10px
```

## Basic Process Flow

1. **AWS Console Login** - Access your AWS account
2. **Navigate to EC2** - Go to EC2 Dashboard  
3. **Launch Instance** - Click "Launch Instance"
4. **Select AMI** - Choose your operating system 🔑 ✅
5. **Choose Instance Type** - Select instance size (t2.micro for free tier) 🔑 ✅
6. **Use Default Settings** - Accept defaults for configuration and storage 📝
7. **Configure Security Group** - Set up basic security rules 🔑 ✅
8. **Review and Launch** - Final review of settings 📝
9. **Key Pair Setup** - Create SSH key pair 🔑 ✅
10. **Download Key Pair** - Save key file securely 🔑 ✅
11. **Verify Running** - Confirm instance is running 🔑 ✅
12. **Connect** - SSH into your running instance 📝

## Prerequisites

- AWS account with EC2 permissions
- Basic understanding of cloud computing
- SSH client for connection
