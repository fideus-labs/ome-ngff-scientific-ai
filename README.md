---
marp: true
theme: default
class: lead
paginate: true
backgroundColor: #fff
color: #333
header: 'OME-NGFF and Scientific AI'
footer: '[![h:40 fideus labs logo](https://fideus-labs.github.io/scientific-ai-omezarr-tutorial/assets/fideus-logo-no-text.svg)](https://fideus.io)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Matt McCormick, PhD | fideus labs | OME-NGFF Workshop 2025'
---

<style>
img[alt~="center"] {
  display: block;
  margin: 0 auto;
}
.small-text {
  font-size: 0.6em;
}
</style>

# Scientific AI and the Future of OME-NGFF
## Intelligent Bioimage Analysis Workflows

**Matt McCormick, PhD**
*fideus labs*

OME-NGFF Workshop 2025

<div class="small-text">

**📜 License:** Content [CC-BY-4.0](https://creativecommons.org/licenses/by/4.0/) | Code [MIT](https://opensource.org/licenses/MIT)

</div>

---

## Today's Vision

**25 minutes of inspiration**

1. **Scientific AI and Your Data** (5 min)
   - Why OME-NGFF for agentic AI

2. **Introduction to the ngff-zarr MCP Server** (10 min)
   - AI-powered bioimage conversion and batch processing

3. **Next Steps You Can Take** (10 min)
   - Improve your scientific throughput, reproducibility, and impact

---

# Part 1: Scientific AI and Your Data
*Why OME-NGFF for Agentic AI*

---

## The AI Revolution in Science

**Large Language Models (LLMs)** are transforming scientific computing:
- 💬 Natural language interfaces to complex tools
- 🧠 Reasoning over scientific data and workflows
- 🤖 **Agentic AI**: Models that can plan, decide, and execute

**The Challenge:** *How do we give AI meaningful access to your scientific imaging data?*

---

## What is Agentic AI?

**Traditional AI:** Question → Answer

**Agentic AI:**
- 🧠 **Context** - Understanding your specific problem
- 🛠️ **Tools** - Access to your scientific software
- 🔄 **Reasoning** - Planning multi-step workflows
- ✅ **Execution** - Actually processing your data

**Result:** AI that understands your science and automates complex analyses

---

## Why OME-NGFF is Perfect for Agentic AI

### ☁️ Cloud-Ready Architecture
* **Chunked storage** - access specific regions without downloading entire datasets
* **Hierarchical structure** - AI can reason about data at multiple scales
* **Open standard** - works everywhere your AI runs

---

## Why OME-NGFF is Perfect for Agentic AI

### 📚 Rich Metadata
* **Spatial information** preserved and queryable
* **Standards-compliant** - AI knows what it's working with
* **Ecosystem of tools** - interoperability enables complex workflows

---

## Why OME-NGFF is Perfect for Agentic AI
### 🌐 Truly Open
* **No vendor lock-in** - your data remains yours
* **Community-driven** - growing ecosystem of tools and support
* **Reproducible science** - data format ensures long-term accessibility

---

## The Power of the Combination

```
Your Scientific Data (OME-NGFF)
        ↓
    AI Agent
   (with tools & context)
        ↓
Automated, Reproducible Workflows
```

**What becomes possible:**
- 🧪 Analyze petabyte-scale datasets in minutes
- 📊 Reproducible computational experiments
- 🎯 Intelligent parameter optimization
- 🚀 Batch processing without manual intervention

---

# Part 2: Introduction to the ngff-zarr MCP Server
*AI-Powered Bioimage Conversion and Batch Processing*

---

## What is the Model Context Protocol (MCP)?

**Universal bridge** between AI assistants and your scientific tools

```
Your AI Assistant (Claude, Qodo, etc.)
        ↕️
    MCP Client
        ↕️
  MCP Server (ngff-zarr)
        ↕️
Your Scientific Data & Tools
```

**Why MCP?**
- ✅ Standard protocol - works with multiple AI platforms
- 🔧 Easy integration - no custom coding required
- 🔄 Bidirectional communication - rich interaction model

---

## The ngff-zarr MCP Server

**What is it?**
* [**ngff-zarr**](https://ngff-zarr.readthedocs.io) is an open-source toolkit for working with OME-NGFF data
* The **ngff-zarr MCP Server** exposes this toolkit to agentic AI systems
* **AI-ready interface** - natural language commands to scientific operations

---

## The ngff-zarr MCP Server
**What can it do?**
- 🔄 **Convert** scientific images (NRRD, TIFF, Nifti, etc.) to OME-Zarr
- ✅ **Validate** OME-Zarr datasets for compliance and interoperability
- 🛠️ **Optimize** compression and chunking for your specific access patterns
- 📝 **Inspect** multiscale pyramids, metadata, and data structure
- 📦 **Batch process** large collections of images with reproducible settings

---

## Real-World Example: Batch Conversion

**Without agentic AI:**
```
Manual process for 50 TIFF files:
1. Write conversion script
2. Optimize parameters (trial & error)
3. Run conversions
4. Verify results
5. Debug failures
⏱️ Hours or days of work
```

---

**With agentic AI + ngff-zarr MCP:**
```
Natural language request:
"Convert my 50 microscopy images to OME-NGFF
with optimal compression for my storage constraints"

AI agent:
1. Analyzes sample image
2. Determines optimal chunking
3. Generates conversion script
4. Executes with progress tracking
5. Reports results
✅ Automated, reproducible, minutes
```

---

## Key Capabilities in Action

### 🤖 Intelligent Conversion
* AI analyzes your image data automatically
* Selects appropriate compression codecs
* Generates multiscale pyramids without artifacts
* Optimizes for your hardware and access patterns

---

## Key Capabilities in Action

### 📊 Analysis and Reporting
* Inspect complex multiscale structures
* Generate processing scripts
* Plan batch operations with resource awareness
* Validate results automatically

---

## The Future of Scientific Image Analysis

**Today:** AI helps with individual tasks

**Tomorrow:** AI orchestrates entire scientific workflows
- 🧪 Multi-step analysis pipelines
- 🎯 Automated optimization and tuning
- 📈 Scalable processing of massive datasets
- 🔬 Knowledge discovery through AI reasoning

**Your role:** Guide the AI with scientific questions, not technical commands

---

# Part 3: Next Steps You Can Take
*Improve Your Scientific Throughput, Reproducibility, and Impact*

---

## Getting Started with OME-NGFF

### 📚 Resources and Documentation

**ngff-zarr Project:**
- 📖 **Documentation:**: https://ngff-zarr.readthedocs.io
  *  Comprehensive guides and API reference
- 📂 **GitHub:** https://github.com/fideus-labs/ngff-zarr

**OME-NGFF Specification:**
- 📋 **NGFF Standard:** https://ngff.openmicroscopy.org
- 📚 **Community:** Open Microscopy Environment (OME)

---

## Tools for Every Scientist

### 🐍 ngff-zarr Python Library
**For computational researchers:**
- Direct programmatic access to conversion and optimization
* Integration with Jupyter notebooks and workflows
* Scientific Python ecosystem compatibility (NumPy, Dask, Xarray)
* Custom analysis pipelines built on OME-NGFF

---

## Tools for Every Scientist

### 🟦 ngff-zarr TypeScript Library
**For web and visualization developers:**
- Browser-based OME-NGFF exploration
* Web applications for image analysis
* Cloud-native deployment options

**📝 Note:** *OME-Zarr in cloud environments* by Eric Perlman this afternoon will cover cloud-based imaging workflows in detail!

---

## ⨍ideus labs: Your Support Partner

**Who we are:**
- 🧬 Biomedical imaging specialists
- 🌟 OME-NGFF ecosystem contributors
- 🤝 Open science advocates

---

## ⨍ideus labs: Your Support Partner

**What we offer:**
- 📚 Training and consultation services
- 🔗 Integration support for your existing workflows

---

## ⨍ideus labs: Your Support Partner

**Connect with us:**
- 📧 Email: [info@fideus.io](mailto:info@fideus.io)
- 🌐 Website: [https://fideus.io](https://fideus.io)
- 📰 Subscribe to our newsletter: [https://fideus.io/subscribe](https://fideus.io/subscribe)
- 🐙 Follow our GitHub: [https://github.com/fideus-labs](https://github.com/fideus-labs)

---

## Your Path Forward

### 🎯 Immediate Actions
1. **Explore** the ngff-zarr documentation and examples
2. **Try** converting a sample image to OME-NGFF
3. **Evaluate** whether OME-NGFF fits your workflow

---

## Your Path Forward

### 🚀 Short-term Goals
1. **Pilot** OME-NGFF adoption in your lab
2. **Integrate** with your existing analysis pipelines
3. **Measure** improvements in efficiency and reproducibility

---

## Your Path Forward

### 📈 Long-term Vision
1. **Scale** your analysis to larger datasets
2. **Leverage** AI and automation for complex workflows
3. **Contribute** back to the community

---

## Key Takeaways

✅ **OME-NGFF** is cloud-ready, open, and built for agentic AI

✅ **MCP Servers** bridge your AI assistants and scientific tools

✅ **ngff-zarr** makes powerful bioimage analysis accessible to everyone

✅ **Your impact multiplies** when you combine AI, open data, and reproducible science

---

## Questions & Discussion

**💡 What we covered:**
- Why OME-NGFF is essential for scientific AI
- How ngff-zarr MCP enables intelligent automation
- Concrete steps to improve your research

**👥 Let's discuss:**
- Your specific imaging challenges
- Integration questions for your workflow
- How OME-NGFF can accelerate your research
