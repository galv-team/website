---
title: Galv
date: 2024-10-23
---

{{< blocks/cover title="Welcome to Galv: a Metadata Secretary for Battery Science" image_anchor="top" height="full" >}}
<a class="btn btn-lg btn-primary me-3 mb-4" href="{{% param live_server_url %}}">
  Check it out <i class="fas fa-rocket ms-2"></i>
</a>
<a class="btn btn-lg btn-secondary me-3 mb-4" href="{{% relref "/docs" %}}">
  Learn more <i class="fas fa-arrow-alt-circle-right ms-2"></i>
</a>
<p class="lead mt-5">
All your cycler data at your fingertips: experiment output, cell details, schedule information, and more...
</p>
{{< blocks/link-down color="info" >}}
{{< /blocks/cover >}}


{{% blocks/lead color="primary" %}}
Galv is a platform for managing Battery Cycler test data. 
Keep your experimental data packaged alongside the experimental metadata so you always know which machine did what to which cell.
{{% /blocks/lead %}}


{{% blocks/section color="dark" type="row" %}}
{{% blocks/feature icon="fa-folder-open" title="Organise your data" %}}
Keep your data together where you can get it from anywhere.
{{% /blocks/feature %}}


{{% blocks/feature icon="fas fa-circle-info" title="Easily view metadata" %}}
Which machine <i class="fas fa-microscope"></i>  

did what <i class="fas fa-clipboard-list"></i>  

to which cell? <i class="fas fa-battery-empty"></i>
{{% /blocks/feature %}}


{{% blocks/feature icon="fas fa-rocket" title="Check it out!" %}}
We run a [live demo server]({{% param live_server_url %}}) where you can try Galv.

You'll have a 100MB file limit and we wipe it on the 3rd of every month.
{{% /blocks/feature %}}


{{% /blocks/section %}}


{{% blocks/section %}}
Components
{.h1 .text-center}

Galv is made of three main components:
- **Galv-Server**: the backend server that manages the data
- **Galv-Client**: the frontend client that you interact with
- **Galv-Harvester**: the data collection tool that sends data to the server

We also have a [Python API]({{% param python_api %}}).
{{% /blocks/section %}}


{{% blocks/section color="dark" %}}
How do I get in on this?
{.h1 .text-center}

{{% /blocks/section %}}

{{% blocks/section type="row" %}}
{{% blocks/feature icon="fas fa-rocket" title="Check it out!" %}}
We run a [live demo server]({{% param live_server_url %}}) where you can try Galv.

You'll have a 100MB file limit and we wipe it on the 3rd of every month.
{{% /blocks/feature %}}

{{% blocks/feature icon="fas fa-graduation-cap" title="Read a tutorial" url="tutorial/" %}}
Learn to use Galv with an easy-to-follow tutorial. We even provide the data.
{{% /blocks/feature %}}


{{% blocks/feature icon="fas fa-book-open" title="Read the docs" url="docs/" %}}
Take a deep dive with our comprehensive documentation.
{{% /blocks/feature %}}

{{% /blocks/section %}}
