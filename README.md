---
marp: true
theme: default
class: lead
paginate: true
backgroundColor: #fff
color: #333
header: 'OME-NGFF and Scientific AI'
footer: '[![h:40 fideus labs logo](https://fideus-labs.github.io/ome-ngff-scientific-ai/assets/fideus-logo-no-text.svg)](https://fideus.io)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Matt McCormick, PhD | ⨍ideus labs | OME-NGFF Workshop 2025'
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
*⨍ideus labs*

OME-NGFF Workshop 2025

<div class="small-text">

**📜 License:** Content [CC-BY-4.0](https://creativecommons.org/licenses/by/4.0/) | Code [MIT](https://opensource.org/licenses/MIT)

</div>

<!--
SPEAKER NOTES - Title Slide (2 minutes)

Welcome and Introduction:
- Introduce yourself warmly
- "And who here has experimented with AI assistants like ChatGPT or Claude in their scientific work?"

Set the stage:
- "Today I want to show you how these two powerful technologies - OME-NGFF and AI - are converging to transform how we work with bioimage data"

Timing: Keep this brief - 2 minutes max. Energy should be high!
-->

---

## Real-life Bioimaging Lab Challenges

**Scenario:** A postdoc just collected 50 microscopy images
- Need to quantify cell populations across treatment conditions
- Segment nuclei, measure fluorescence intensity, compare to controls
- Generate statistical analysis and publication-quality figures

<!--
SPEAKER NOTES - The Challenge (0.5 minutes)

Make it visceral:
- "Let me start with a situation you may have experienced..."
- "The postdoc is excited - finally got those microscopy results"
- "50 beautiful images, now you just need the quantification..."

-->
---

## Real-life Bioimaging Lab Challenges

**Without AI:**
```
Week 1: Write analysis scripts, debug edge cases
Week 2: Batch process, fix failures, re-run
Week 3: Statistical analysis, figure generation
⏱️ 3+ weeks of precious postdoc time
```

**With AI + OME-NGFF:**
```
"Analyze these 50 images: segment DAPI-stained nuclei,
quantify GFP intensity per cell, compare treated vs control,
and generate summary statistics with publication figures"
✅ Results in hours, fully reproducible
```

<!--
SPEAKER NOTES - The Challenge (1.5 minutes)

The old way:
- "So they spend the next THREE WEEKS wrestling with analysis"
- "Writing scripts, debugging when Image Number 23 has different dimensions"
- "Re-running everything because they forgot to save parameters"
- "This is the reality we regularly experience"

The new way:
- "Now imagine instead - they just DESCRIBE what they need"
- "Natural language, like talking to a collaborator"
- "The AI agent provides transformative technical assistance"
- "Hours instead of weeks"

Impact:
- "That's three weeks your postdoc gets back for actual science"
- "Three weeks closer to publication"
- "And it's fully reproducible - no 'what parameters were used?' six months later"

Question:
- "How many postdoc-weeks would YOUR lab save?"
- Let that sink in before moving on

Timing: 1.5 minutes - this is your hook!
-->

---

## Today's Vision

**25 minutes of inspiration**

1. **Scientific AI and Your Data** (5 min)
   - Why OME-NGFF for agentic AI

2. **Introduction to the ngff-zarr MCP Server** (10 min)
   - AI-powered bioimage conversion and batch processing

3. **Next Steps You Can Take** (10 min)
   - Improve your scientific throughput, reproducibility, and impact

<!--
SPEAKER NOTES - Agenda (1 minute)

Roadmap:
- "We have 25 minutes together, so let's make them count"
- Point to each section as you describe it
- "First, I'll show you WHY OME-NGFF and AI are a perfect match"
- "While we ARE admittedly only in the beginning stages of SCIENTIFIC AI, we will dive into a REAL tool you can use today - the ngff-zarr MCP server"
- "Finally, we will look at concrete steps YOU can take NOW to get started"

Timing: 1 minute - keep it moving!
-->

---

# Part 1: Scientific AI and Your Data
*Why OME-NGFF for Agentic AI*

<!--
SPEAKER NOTES - Part 1 Transition (30 seconds)

Transition:
- "Let's start with the big picture - what's happening in AI right now"
- Energy shift: move from logistics to inspiration
- "Let's examine why OME-NGFF is ideal for agentic scientific AI"

Timing: Quick transition - 30 seconds
-->

---

## The AI Revolution in Science

**Large Language Models (LLMs)** are transforming scientific computing:
- 💬 Natural language interfaces to complex tools
- 🧠 Reasoning over scientific data and workflows
- 🤖 **Agentic AI**: Models that can plan, decide, and execute

**The Challenge:** *How do we give AI meaningful access to your scientific imaging data?*

<!--
SPEAKER NOTES - AI Revolution (1.5 minutes)

Context setting:
- "We're in the middle of a profound shift in how we interact with computers"
- "Most folks have used chatbots to search for information or generate narritive text"
- "But here's what's NEW - we're moving beyond chatbots to AGENTS"

Key point - AGENTIC AI:
- Emphasize the difference: "Not just answering questions, but actually DOING work"
- "Planning multiple steps, using tools, making decisions"

The challenge:
- "But here's the problem - how does AI -- text-based large language models -- actually WORK with YOUR imaging DATA?"
- "That's where OME-NGFF comes in..."
- Pause for effect before moving on

Timing: 1.5 minutes - this is foundational!
-->

---

## What is Agentic AI?

*Traditional AI:* **Question → Answer**
*Agentic AI:* **Goal → Outcome**

* 🧠 **Context** - Understanding your specific problem
* 🛠️ **Tools** - Access to your scientific software
* 🔄 **Reasoning** - Planning multi-step workflows
* ✅ **Execution** - Actually processing your data

**Result:** AI that understands your science and automates complex analyses

<!--
SPEAKER NOTES - Agentic AI Definition (1.5 minutes)

Break it down clearly:
- "Let me make this concrete with an example..."
- Walk through each element:
  * Context: "The AI knows about YOUR specific microscope, YOUR file formats"
  * Tools: "It can actually run conversion software, optimization scripts"
  * Reasoning: "It plans: first validate, then convert, then optimize"
  * Execution: "And it DOES it - not just tells you how"

Engage with questions:
- "Think about your last batch conversion task - how long did it take?"
- "What if you could just DESCRIBE what you need and have it happen?"

Make it tangible:
- "This isn't science fiction - I'm going to show you how this works in 10 minutes"

Timing: 1.5 minutes - enthusiasm is key here!
-->

---

## Why OME-NGFF is Perfect for Agentic AI

### ☁️ Cloud-Ready Architecture
* **Chunked storage** - access specific regions without downloading entire datasets
* **Hierarchical structure** - AI can reason about data at multiple scales
* **Standard web interfaces** - works everywhere your AI runs

<!--
SPEAKER NOTES - OME-NGFF + AI Part 1: Cloud Architecture (1 minute)

Connect to AI capabilities:
- "Now here's where it gets interesting - OME-NGFF was DESIGNED for exactly this kind of intelligent access"

Cloud-ready chunked storage:
- "The AI doesn't need to download terabytes - it can grab just the chunks it needs"

Hierarchical structure:
- "Like reading specific chapters of a book instead of the whole library"

Web-friendly, AI-tool-calling friendly interface:
- "AI can request just the metadata it needs - dimensions, spacing, coordinate systems"
- "Then fetch only the specific data regions required for analysis"
- "Works seamlessly whether your data is local or in the cloud"
- "The same HTTP-based interface works everywhere - perfect for AI tool integration"

Timing: 1 minute - keep pace brisk
-->

---

## Why OME-NGFF is Perfect for Agentic AI

### 📚 Rich Metadata
* **Spatial information** preserved and queryable
* **Standards-compliant** - AI knows what it's working with
* **Ecosystem of tools** - interoperability enables complex workflows

<!--
SPEAKER NOTES - OME-NGFF + AI Part 2: Metadata (45 seconds)

Rich metadata advantage:
- "But storage format isn't enough - the AI needs to UNDERSTAND your data"
- "OME-NGFF embeds all the spatial metadata, calibration, channel information"

Standards matter:
- "Because it's standards-compliant, the AI can make intelligent assumptions"
- "It knows what 'microns' means, what coordinate systems to use"

Ecosystem:
- "And it can chain together multiple tools that all speak OME-NGFF"

Timing: 45 seconds - building momentum
-->

---

## Why OME-NGFF is Perfect for Agentic AI
### 🌐 Truly Open
* **No vendor lock-in** - your data remains yours
* **Community-driven** - growing ecosystem of tools and support
* **Reproducible science** - data format ensures long-term accessibility

<!--
SPEAKER NOTES - OME-NGFF + AI Part 3: Open Standards (45 seconds)

Open science connection:
- "And here's what I love most - this is TRULY open"
- "Your data isn't trapped in some proprietary format"
- "The AI tools we build today will work with your data in 10 years"

Emphasize community:
- "You're JOINING a COMMUNITY, not buying into a vendor"

Timing: 45 seconds
-->

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
* 🧪 Analyze petabyte-scale datasets in minutes
* 📊 Reproducible computational experiments
* 🎯 Intelligent parameter optimization
* 🚀 Batch processing without manual intervention

<!--
SPEAKER NOTES - The Combination (1 minute)

Bring it together:
- "So let's put this together - what does this MEAN for your research?"
- Point to the diagram: "Data format + AI capability = transformation"

Make it real:
- "Imagine: 'Convert these 1000 microscopy images, optimize for cloud storage, and validate the results'"
- "Just describe it, and it happens"
- "No bash scripts, no parameter tuning, no debugging at 2am"

Each bullet:
- Petabyte: "Datasets that would take weeks become lunch-break tasks"
- Reproducible: "Everything documented, every parameter logged automatically"
- Optimization: "The AI tries different approaches and finds what works best"
- Batch: "Your weekend work becomes 10 minutes on Monday morning"

Pause:
- "This is the vision."
- "We are not there yet."
- "But we ARE on our awy there! Now let me show you how this ACTUALLY works..."

Timing: 1 minute - this is the payoff slide!
-->

---

![h:150 center ngff-zarr logo](https://fideus-labs.github.io/scientific-ai-omezarr-tutorial/assets/ngff-zarr-logo.png)

# Part 2: Introduction to the ngff-zarr MCP Server
*AI-Powered Bioimage Conversion and Batch Processing*

<!--
SPEAKER NOTES - Part 2 Transition (30 seconds)

Energy shift:
- "Okay, enough theory - let's get practical"
- "I'm going to introduce you to a free and open source tool available TODAY"
- Check time - should be around 8-9 minutes in

Timing: 30 seconds - quick transition
-->

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

<!--
SPEAKER NOTES - MCP Introduction (1.5 minutes)

What is MCP:
- "The Model Context Protocol (MCP) is like USB for AI - a universal connector"
- "Developed by Anthropic, but it's open and vendor-neutral"
- Point to diagram: "Your AI assistant connects to scientific tools through this protocol"

Why this matters:
- "You don't have to choose between AI platforms"
- "Works with Claude, with Cursor, with GitHub Copilot, with dozens of existing agent platforms and with future AI systems"
- "The same MCP server works with all of them"

Easy integration:
- "And here's the beautiful part - YOU don't have to code the integration"
- "The MCP server does all the heavy lifting"

Question:
- "Anyone here familiar with MCP already?"
- If yes: "Great! You know where this is going"
- If no: "You're about to see how simple it is"

Timing: 1.5 minutes - this is new to most people
-->

---

## The ngff-zarr MCP Server

![h:150 center ngff-zarr logo](https://fideus-labs.github.io/scientific-ai-omezarr-tutorial/assets/ngff-zarr-logo.png)

**What is it?**
* [**ngff-zarr**](https://ngff-zarr.readthedocs.io) is an open-source toolkit for working with OME-NGFF data
* The **ngff-zarr MCP Server** exposes this toolkit to agentic AI systems
* **AI-ready interface** - natural language commands to scientific operations

<!--
SPEAKER NOTES - ngff-zarr Introduction (1 minute)

Introduce the tool:
- "This is ngff-zarr - our contribution to the OME-NGFF ecosystem"
- "It's a Python toolkit we've been developing at fideus labs"
- "And now it has an MCP server that lets AI systems use it"

What this means:
- "You can talk to your AI assistant: 'Convert this image to OME-NGFF'"
- "And behind the scenes, the MCP server translates that to ngff-zarr commands"
- "Then executes them and reports back results"

Emphasize:
- "Completely open source - MIT licensed"
- "Link is in the slides"

Timing: 1 minute
-->

---

## The ngff-zarr MCP Server
**What can it do?**
* 🔄 **Convert** scientific images (NRRD, TIFF, Nifti, etc.) to OME-Zarr
* ✅ **Validate** OME-Zarr datasets for compliance and interoperability
* 🛠️ **Optimize** compression and chunking for your specific access patterns
* 📝 **Inspect** multiscale pyramids, metadata, and data structure
* 📦 **Batch process** large collections of images with reproducible settings

<!--
SPEAKER NOTES - Capabilities (1.5 minutes)

Go through each capability with examples:

Convert:
- "Supports all the formats you're probably using - TIFF, NRRD, Nifti, and more"
- "AI can figure out the right conversion settings for your data"

Validate:
- "Check if your OME-Zarr files are spec-compliant"
- "Catch issues before you publish or share data"

Optimize:
- "This is powerful - AI can test different compression and chunking strategies"
- "Find the sweet spot for YOUR access patterns"

Inspect:
- "Get detailed information about multiscale structure"
- "Understand what's actually in your data"

Batch process:
- "Generate bespoke batch processing scripts for large collections of images with reproducible settings"

Timing: 1.5 minutes - let each capability sink in
-->

---

## Real-World Example: Quantitative Analysis Pipeline

**Remember our postdoc with 50 images?**

**Without agentic AI:**
```
Traditional manual workflow:
1. Convert images to working format (troubleshoot compatibility)
2. Write segmentation script (tune parameters per image)
3. Extract measurements (debug data export)
4. Statistical analysis (wrangle data formats)
5. Generate figures (iterate on visualization)
6. Document everything (if you remember what you did)
⏱️ 2-3 weeks of iteration and debugging
```

<!--
SPEAKER NOTES - Before AI Example (1.5 minutes)

Bring back the scenario:
- "Remember our postdoc? Let's walk through their typical workflow..."
- Make it painful but relatable

Step by step pain:
1. Format conversion:
   - "First hurdle - get images into format the analysis tools can read"
   - "Proprietary microscope format doesn't work with open ecosystem tools"
   - "Spend half a day on format conversion alone"

2. Segmentation:
   - "Then the real work - write segmentation code"
   - "Parameters that work for Image Number 1 fail on Image Number 15"
   - "Back to parameter tuning, over and over"

3. Measurements:
   - "Finally getting data out - but wait, export format issues"
   - "CSV? JSON? How to link measurements to metadata?"

4. Statistics:
   - "Now wrangle everything into R or Python for stats"
   - "More data format conversion, more potential for errors"

5. Figures:
   - "Generate plots, realize you need different groupings"
   - "Re-run everything from step 3"

6. Documentation:
   - "And did you write down all those parameters?"
   - "Good luck reproducing this in 6 months"

The reality:
- "This is 2-3 weeks of a postdoc's time"
- "And that's if everything goes relatively smoothly"
- "We've all been there"

Timing: 1.5 minutes - make them FEEL the pain
-->

---

**With agentic AI + ngff-zarr MCP:**
```
Natural language request:
"Analyze these 50 microscopy images: segment DAPI-stained nuclei,
quantify GFP intensity per cell, compare treated vs control groups,
and generate summary statistics with publication figures"

AI agent:
1. Converts to OME-NGFF (optimal format selection)
2. Performs segmentation (auto-tunes parameters)
3. Extracts measurements (structured metadata)
4. Runs statistical comparisons (appropriate tests)
5. Generates figures (publication-ready)
6. Documents entire workflow (fully reproducible)
✅ Results in hours, not weeks - fully automated and documented
```

<!--
SPEAKER NOTES - After AI Example (1.5 minutes)

The contrast:
- "Now watch what happens with our agentic AI future..."
- Read the natural language request slowly

AI does the work:
- "The agent helps us:"
- "Analyze a sample to understand your data"
- "Determine optimal settings based on your constraints"
- "Generates AND RUNS the conversion"
- "Tracks progress, handles errors"
- "Gives you a summary when done"

The magic moment:
- "From hours or days to MINUTES"
- "From error-prone to reproducible"
- "From tedious to... well, you just describe what you want"

Reality check:
- "Now, this isn't magic - the AI CAN still make mistakes"
- "But it's MUCH faster to review and correct than to do it all from scratch"
- "And the agent can document everything as you work with the agent"

Timing: 1.5 minutes - this is the "wow" moment
-->
---

## 🛠️ In Practice: AI-Powered Conversion

<!--
SPEAKER NOTES - In Practice Intro (15 seconds)

Quick transition:
- "Now let me show you what this looks like in practice"
- "Three quick examples of natural language to results"

Timing: 15 seconds - just a bridge
-->

---

### 💬 Convert a bioimage with AI assistance

Put the agent to work!

In chat:
```
Convert the vs_male.nrrd file to OME-Zarr format and
find the optimal compression codec for this type of data.
```

**✨ [Watch the AI agent](https://fideus-labs.github.io/scientific-ai-omezarr-tutorial/assets/ai-convert-output.png):**
1. 🔍 Analyze the input file
2. 🎯 Select appropriate parameters
3. ⚙️ Execute the conversion
4. 📊 Report optimization results

<!--
SPEAKER NOTES - Convert Example (45 seconds)

Show the simplicity:
- "Look at this - natural language, plain English"
- "No command-line flags, no config files"
- Point to the chat message: "Just describe what you want"

Demo reference:
- Click the link
- "We see the agent's reasoning process"

What happens:
- "The AI agent takes over from here"
- "Analyzes the file - dimensions, data type, characteristics"
- "Picks appropriate parameters automatically"
- "Runs the conversion and tests different codecs"
- "Tells you which one worked best and why"

Timing: 45 seconds
-->

---

### 💬 Examine OME-Zarr contents

**Ask the AI to explore:**

```
Examine the contents of carp.ome.zarr and tell me
about its structure, dimensions, and metadata
```

**✨ [The AI agent will](https://fideus-labs.github.io/scientific-ai-omezarr-tutorial/assets/ai-examine-contents-output.png):**
- 🔍 Inspect multiscale levels
- 📏 Report spatial metadata
- 🧩 Analyze chunk structure
- ✨ Suggest next steps

<!--
SPEAKER NOTES - Examine Example (45 seconds)

Beyond conversion:
- "It's not just for conversion - also for exploration"
- "Ask questions about your data in plain language"

Demo reference:
- Click the link

What you get:
- "The AI inspects the multiscale pyramid structure"
- "Reports all the spatial metadata - spacing, units, coordinates"
- "Analyzes how the data is chunked and compressed for efficient handling of petabyte datasets"
- "In the future, it could even suggest what you might want to do next"

Use case:
- "Great for validating datasets before sharing"
- "Or understanding data someone shared with you"

Timing: 45 seconds
-->

---

### 💬 Generate batch script

**Scale up with AI automation:**

```
I have a folder of 50 similar NRRD files.
Generate a Python script to batch convert them all
to OME-Zarr with the same optimal settings
```

**✨ [The AI agent creates](https://fideus-labs.github.io/scientific-ai-omezarr-tutorial/assets/ai-generate-batch-script-output.png):**
- 🐍 Complete Python script
- ⚠️ Error handling
- 📈 Progress reporting
- 🎯 Optimized parameters from previous analysis

<!--
SPEAKER NOTES - Batch Script Example (45 seconds)

Scaling up:
- "And here's where it gets really powerful"
- "Once you've tested on one file, scale to many"

Demo reference:
- Click the link

What it generates:
- "It produces a complete, runnable Python script"
- "Includes proper error handling - won't crash on bad files"
- "Progress output so you know where you are"
- "Uses the optimal settings it learned from your test conversion"

Reproducibility:
- "Now you have a script you can run again"
- "Share with colleagues, include in your methods"
- "Fully documented, reproducible workflow"

Timing: 45 seconds
-->

---

## Key Capabilities in Action

### 🤖 Intelligent Conversion
* AI analyzes your image data automatically
* Selects appropriate compression codecs
* Generates multiscale pyramids without artifacts
* Optimizes for your hardware and access patterns

<!--
SPEAKER NOTES - Intelligent Conversion (45 seconds)

What makes it intelligent:
- "So what makes this 'intelligent' and not just scripted?"
- "The AI adapts to YOUR specific data"

Examples:
- "Looks at dimensions, bit depth, noise patterns"
- "Chooses blosc for speed or zstd for compression based on your needs"
- "Generates clean multiscale pyramids automatically"
- "Optimizes for local disk vs cloud access patterns"

Bottom line:
- "It makes informed decisions, not just defaults"

Timing: 45 seconds
-->

---

## Key Capabilities in Action

### 📊 Analysis and Reporting
* Inspect complex multiscale structures
* Generate processing scripts
* Plan batch operations with resource awareness
* Validate results automatically

<!--
SPEAKER NOTES - Analysis and Reporting (45 seconds)

Beyond conversion:
- "Also handles inspection, validation, planning"

Key features:
- "Describes your multiscale structure in detail"
- "Generates scripts for reproducibility"
- "We are TRANSFERRING some of the BURDEN of REPRODUCIBILITY from a busy postdoc to the AI agent"
- "Validates outputs before you share"

Quick check:
- Check time - should be around 18-19 minutes

Timing: 45 seconds
-->

---

## The Future of Scientific Image Analysis

**Today:** AI agents help with format conversion and optimization

**Tomorrow:** AI agents assist entire scientific workflows
- 🧪 Multi-step analysis pipelines
- 🎯 Automated optimization and tuning
- 📈 Scalable processing of massive datasets
- 🔬 Knowledge discovery through AI reasoning

**Your role:** Guide the AI with scientific questions, not technical commands

<!--
SPEAKER NOTES - Future Vision (1 minute)

Look ahead:
- "This is just the beginning - where is this going?"

Today vs tomorrow:
- "Right now, the helps with format conversion"
- "But we can have a future where you'll have advanced assistance through an entire analysis workflow"
- "'Take these images, segment the cells, quantify fluorescence, compare to controls, generate publication figures'"

Examples:
- Multi-step: "Chain together preprocessing, analysis, visualization"
- Optimization: "AI tries different parameters, finds best results"
- Discovery: "And, the agent may even notice patterns you might have missed"

Your role shift:
- "You become the scientist who asks questions"
- "Not the programmer who debugs bash scripts"
- "Focus on WHAT you want to know, not HOW to compute it"

Timing: 1 minute - inspire them!
-->

---

# Part 3: Next Steps You Can Take
*Improve Your Scientific Throughput, Reproducibility, and Impact*

<!--
SPEAKER NOTES - Part 3 Transition (30 seconds)

Final section:
- "We're in the home stretch - let's talk about YOUR next steps"
- Check time - should be around 19-20 minutes
- "How do you actually GET STARTED with this?"

Timing: 30 seconds
-->

---

## Your Path Forward

### 🎯 Immediate Actions
1. **Explore** the ngff-zarr documentation and examples
2. **Try** converting a sample image to OME-NGFF
3. **Evaluate** whether OME-NGFF fits your workflow

<!--
SPEAKER NOTES - Immediate Actions (45 seconds)

This week:
- "Okay, concrete actions you can take THIS WEEK"

Explore:
- "Tonight in your hotel room - browse the docs"
- "Look at the examples, see if they match your use cases"

Try it:
- "Tomorrow - take ONE image and convert it"
- "Just pip install ngff-zarr and try the command line interface"
- "5 minutes to get started"

Evaluate:
- "Think about YOUR workflow - where would this help?"
- "What's your biggest pain point with image formats?"
- "Could OME-NGFF solve it?"

Timing: 45 seconds
-->

---

## Your Path Forward

### 🚀 Short-term Goals
1. **Pilot** OME-NGFF adoption in your lab
2. **Integrate** with your existing analysis pipelines
3. **Measure** improvements in efficiency and reproducibility

<!--
SPEAKER NOTES - Short-term Goals (45 seconds)

Next month or two:
- "Over the next month or two, here's what success looks like"

Pilot:
- "Start small - one project, one dataset"
- "Learn the workflow without disrupting everything"
- "Get your team comfortable with the tools"

Integrate:
- "Connect OME-NGFF to your existing analysis"
- "You don't have to rebuild everything"
- "It should ENHANCE your workflow, not replace it"

Measure:
- "And track the benefits - time saved, errors reduced"

Question:
- "What would be a good pilot project in YOUR lab?"

Timing: 45 seconds
-->

---

## Your Path Forward

### 📈 Long-term Vision
1. **Scale** your analysis to larger datasets
2. **Leverage** AI and automation for complex workflows
3. **Contribute** back to the community

<!--
SPEAKER NOTES - Long-term Vision (45 seconds)

Looking ahead:
- "And looking 6-12 months out, imagine..."

Scale:
- "Datasets that seemed impossible become routine"
- "Multi-terabyte analyses running in the cloud"
- "Your science limited by questions, not infrastructure"

Leverage AI:
- "AI assistants handling the grunt work"
- "You focus on interpretation and discovery"
- "And you have automation that actually works"

Contribute:
- "Here's what's BEAUTIFUL - as you build tools and workflows"
- "Share them back with the community"
- "Make OME-NGFF better for everyone"
- "That's how open science works"

Timing: 45 seconds
-->

---
## Tools for Every Scientist

### 🐍 ngff-zarr Python Library
**For computational researchers:**
- Direct programmatic access to conversion and optimization
* Integration with Jupyter notebooks and workflows
* Scientific Python ecosystem compatibility (NumPy, Dask, Xarray)
* Custom analysis pipelines built on OME-NGFF

**📝 Note:** *OME-Zarr in cloud environments* by Eric Perlman this afternoon will cover cloud-based imaging workflows in detail!

<!--
SPEAKER NOTES - Python Library (45 seconds)

For Python users:
- "Even if you don't want to use AI assistants yet"
- "If you're a Python person, we've got you covered"
- "The library integrates seamlessly with your existing stack"
- "The package has over 15,000 monthly downloads from PyPI and a dozen contributors"

Jupyter:
- "Works great in notebooks - try it interactively"
- "See the examples in our docs"

Ecosystem:
- "Built on NumPy, works with Dask for parallel processing"
- "Xarray for labeled arrays"
- "Familiar tools, with OME-NGFF superpowers"

Custom pipelines:
- "Use it as a building block for your own workflows"
- "Not locked into our way of doing things"

Cross-reference:
- "And speaking of cloud - Eric Perlman's talk this afternoon"
- "Will go deep on cloud workflows"
- "Highly recommended!"

Timing: 45 seconds
-->

---

## Tools for Every Scientist

### 🟦 ngff-zarr TypeScript Library
**For web and visualization developers:**
- Browser-based OME-NGFF exploration
* Web applications for image analysis
* Cloud-native deployment options

<!--
SPEAKER NOTES - TypeScript Library (45 seconds)

Web developers:
- "We also have a TypeScript/JavaScript version"
- "Build web apps, visualization tools"

Browser-based:
- "Run OME-NGFF analysis right in the browser"
- "No server needed for many tasks"

Cloud deployment:
- "Deploy to Vercel, Netlify, anywhere"
- "Share interactive visualizations with collaborators"

Timing: 45 seconds
-->

---

## ⨍ideus labs

**Who we are:**
- 🧬 Biomedical imaging specialists
- 🌟 OME-NGFF ecosystem contributors
- 🤝 Open science advocates

**What we offer:**
- 📚 Training and consultation services
- 🔗 Integration support for your existing workflows

**Connect:** 📧 Email: [info@fideus.io](mailto:info@fideus.io) 🌐 Website: [https://fideus.io](https://fideus.io)
<!--
SPEAKER NOTES - fideus Intro (30 seconds)

Introduce fideus:
- "Quick word about who we are"
- "We're fideus labs - this is our passion"

What we do:
- "We specialize in biomedical imaging infrastructure"
- "We're active contributors to OME-NGFF and related tools"
- "We're committed to open science and open source"

Not a sales pitch:
- "We're here to help the community"
- "Whether that's with us or on your own"
- "Happy to chat after the talk or during breaks"

Timing: 30 seconds - brief and humble
-->

---


## Key Takeaways

✅ **OME-NGFF** is cloud-ready, open, and built for agentic AI

✅ **MCP Servers** bridge your AI assistants and scientific tools

✅ **ngff-zarr** makes powerful bioimage analysis accessible to everyone

✅ **Your impact multiplies** when you combine AI, open data, and reproducible science

<!--
SPEAKER NOTES - Key Takeaways (1 minute)

Summarize the message:
- "Let me leave you with four key points"

Read each one with emphasis:
1. "OME-NGFF:"
   - "This format was DESIGNED for the AI era"
   - "Cloud-ready, open, future-proof"

2. "MCP:"
   - "The bridge that makes AI assistants actually useful"
   - "Standard protocol, works everywhere"

3. "ngff-zarr:"
   - "Tools you can use TODAY"
   - "Free, open source, ready to go"

4. Your impact:
   - "This isn't just about convenience"
   - "It's about MULTIPLYING your scientific impact"
   - "Better reproducibility, broader collaboration, faster discovery"

Pause:
- "These four things together are transformative"

Timing: 1 minute - should be at ~24 minutes total
-->

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

<!--
SPEAKER NOTES - Questions & Discussion (1+ minute, flexible)

Final thoughts:
- "That's what I wanted to share with you today"
- "We should have a few minutes for questions"
- Check actual time - adjust accordingly

Open the floor:
- "What questions do you have?"
- "Anyone have a specific use case you want to discuss?"
- "How much time is a postdoc going to spend on the next 50 images?"

Be ready for common questions:
- Performance compared to other formats
- Existing tool compatibility
- Learning curve for teams
- Cloud storage costs
- Production readiness

Encourage engagement:
- "Don't be shy - if you're wondering it, others are too"
- "I'll also be around during breaks if you want to chat more"

Thank them:
- "Thank you for your attention"
- "Excited to see what you build with these tools"
- "Let's make bioimage analysis better together"

Timing: Flexible - use remaining time, but don't run over!
-->

---

## Getting Started with OME-NGFF

### 📚 Resources and Documentation

**ngff-zarr Project:**
- 📖 **Documentation:**: https://ngff-zarr.readthedocs.io
  -  Comprehensive guides and API reference
- 📂 **GitHub:** https://github.com/fideus-labs/ngff-zarr

**OME-NGFF Specification:**
- 📋 **NGFF Standard:** https://ngff.openmicroscopy.org
- 📚 **Community:** Open Microscopy Environment (OME)

<!--
SPEAKER NOTES - Resources (45 seconds)

Point to resources:
- "As we go through questions and discussion, everything I've shown you is documented here"

ngff-zarr docs:
- "Start here - we have tutorials, examples, API docs"
- "Including documentation on the ngff-zarr MCP server setup"

OME-NGFF spec:
- "For the deep dive into the format specification"
- "This is the authoritative source"

Community:
- "Join the OME community - forums, mailing lists"
- "People are friendly and helpful!"

Timing: 45 seconds - practical and actionable
-->
