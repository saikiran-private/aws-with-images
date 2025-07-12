# Documentation Consistency Rules & Guidelines

This file contains the standardized rules and templates for creating consistent markdown documentation with Mermaid diagrams.

## 📋 **Markdown File Creation Rules**

### **1. File Structure & Naming**
- Use descriptive filenames: `Basic-[process-name]-creation.md`
- Keep content minimal and focused
- Structure: Title → Overview → Diagram → Process Flow → Prerequisites

### **2. Mermaid Diagram Standards**
```markdown
## [Process Name] Flow Diagram

```mermaid
flowchart TD
    A[Start: Process Name] -----> B[Next Step]
    B -----> C[Another Step]
    
    %% Image references with actual dimensions
    A@{ img: "https://raw.githubusercontent.com/[username]/[repo]/main/images/[image-name].png", h: [actual-height], w: [actual-width], pos: "t"}
    
    %% Styling - large fonts and colors
    style A fill:#e1f5fe,font-size:30px
    style B fill:#c8e6c9,font-size:30px
    
    %% Arrow styling - thick and long
    linkStyle default stroke-width:10px
    linkStyle 0 stroke-width:10px
```

### **3. Image Handling Rules**
- **Get actual dimensions**: Use `file images/*.png` command to get real image sizes
- **Use exact dimensions**: Always use `h: [actual-height], w: [actual-width]`
- **Position images on top**: Always use `pos: "t"`
- **GitHub raw URLs**: Use `https://raw.githubusercontent.com/[username]/[repo]/main/images/[filename]`

### **4. Visual Styling Standards**
- **Font size**: `font-size:30px` for all nodes
- **Arrow thickness**: `stroke-width:10px` for all arrows
- **Arrow length**: Use `----->` (5 dashes) for longer arrows
- **Colors**: 
  - Start nodes: `fill:#e1f5fe` (light blue)
  - Key steps with screenshots: `fill:#c8e6c9` (light green)
  - Regular nodes: Just `font-size:30px`

### **5. Content Organization Rules**
- **Remove unnecessary steps**: Skip default configuration steps
- **Focus on core concepts**: Only include steps that teach something important
- **Screenshot priority**: Choose screenshots that won't become obsolete
- **Bold commands**: Use `**command**` for terminal commands
- **File extensions**: Be specific (`.pem`, not `<keypair>`)

### **6. Process Flow Guidelines**
- **Numbered list**: Use 1-11 steps maximum
- **Status indicators**: Use 🔑 ✅ for steps with screenshots, 📝 for documented steps
- **Action-oriented**: Start each step with action verbs
- **Specific instructions**: Include actual commands where helpful

### **7. Screenshot Selection Strategy**
- **Future-proof**: Choose concepts that rarely change
- **Essential only**: 5-6 critical screenshots maximum
- **Core concepts**: AMI selection, instance types, security groups, key pairs, final state
- **Skip UI-heavy steps**: Don't screenshot every configuration page

## 🎯 **Quick Prompt Template for Future Projects**

```
Create a [process-name] guide with these requirements:

STRUCTURE:
- Minimal markdown file: Title → Overview → Mermaid Diagram → Process Flow → Prerequisites
- Remove unnecessary steps, focus on core concepts only

MERMAID DIAGRAM:
- Use flowchart TD format
- Long arrows: -----> (5 dashes)
- Thick arrows: stroke-width:10px
- Large fonts: font-size:30px
- Colors: #e1f5fe for start, #c8e6c9 for key steps
- Images: Use actual dimensions with pos: "t"

CONTENT:
- 5-6 critical screenshots maximum
- Bold commands with specific file extensions
- Action-oriented numbered steps
- Status indicators: 🔑 ✅ for screenshots, 📝 for documented

SCREENSHOTS:
- Get actual dimensions using file command
- Choose future-proof concepts only
- GitHub raw URLs for images
```

## 🔄 **Consistency Checklist**
- [ ] File uses descriptive naming convention
- [ ] Mermaid diagram has 30px fonts and 10px arrows
- [ ] Images use actual dimensions with `pos: "t"`
- [ ] Only 5-6 essential screenshots included
- [ ] Commands are bold with specific file extensions
- [ ] Process flow is action-oriented and concise
- [ ] Colors follow the established scheme

## 📁 **File Organization**
- Main documentation file: `Basic-[process-name]-creation.md`
- Images folder: `images/`
- Consistency rules: `DOCUMENTATION_CONSISTENCY_RULES.md` (this file)

## 🎨 **Color Scheme Reference**
- **Start nodes**: `#e1f5fe` (Light blue)
- **Key steps with screenshots**: `#c8e6c9` (Light green)
- **Regular nodes**: No fill, just font styling

## 🖼️ **Image Requirements**
- **Format**: PNG files
- **Naming**: Descriptive names (e.g., `ami-selection.png`)
- **Dimensions**: Use actual image dimensions
- **Position**: Always `pos: "t"` (top)

## 📝 **Example Template**

```markdown
# Basic [Process Name] Guide

This file contains a simplified guide for [process description] with step-by-step screenshots.

## Overview

The guide follows a streamlined approach for [process], focusing on essential steps with default configurations.

## [Process Name] Flow Diagram

```mermaid
flowchart TD
    A[Start: Process] -----> B[Step 1]
    B -----> C[Step 2]
    
    A@{ img: "https://raw.githubusercontent.com/username/repo/main/images/step1.png", h: 430, w: 1270, pos: "t"}
    
    style A fill:#e1f5fe,font-size:30px
    style B fill:#c8e6c9,font-size:30px
    
    linkStyle default stroke-width:10px
    linkStyle 0 stroke-width:10px
```

## Basic Process Flow

1. **Start Process** - Description 🔑 ✅
2. **Step 1** - Description 🔑 ✅
3. **Step 2** - Description 📝

## Prerequisites

- Required items
- Basic understanding
- Tools needed
```

## 🚀 **Quick Start Commands**

```bash
# Get image dimensions
file images/*.png

# Check git status
git status

# Add and commit changes
git add .
git commit -m "Add [process-name] guide with Mermaid diagram"

# Push to GitHub
git push origin main
```

---

**Note**: This file serves as your reference guide. Keep it in your project root and refer to it when creating new documentation to maintain consistency across all your guides. 