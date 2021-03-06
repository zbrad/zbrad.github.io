---
layout: post
title: How to use the Oxford OCR API with Powershell
categories: tools
tags: [powershell,oxford,ocr]
date: 2015-06-29
image:
  feature: psoxford/oxford.jpg
  credit: 
  creditlink: https://zbrad.github.io/

---

I recently had a need to use OCR on an existing image, and a teamate suggested using
the new [Oxford APIs](https://www.projectoxford.ai/doc/general/overview){:target="_blank"}. This was a result of my afternoon
quick hack, but rolled up into a Powershell cmdlet that could be reused by others.

## Setting up the Oxford APIs for use ##

To quickly get up to speed, I followed the descriptions [here](https://www.projectoxford.ai/doc/general/subscription-key-mgmt) which outline the steps as:

- Select the API you wish to use
  - I navigated to [Computer Vision APIs](https://www.projectoxford.ai/vision) and selected the "Sign Up" button.
- This will bring up the Azure portal, select the marketplace
  ![](/images/psoxford/select-from-marketplace.png)
  you will have to option of naming your service, I chose *VisionApi*
  ![](/images/psoxford/portal.png)
  The "purchase" is free, and shows up as an Azure Marketplace offering. (Note that you may need to scroll down the listing of services in the Azure portal.
- When you are presented with the "dashboard" for the marketplace, select the "Manage" option
  ![](/images/psoxford/visionapi_dashboard.png)
- You will now see your subscriptions with key information hidden.  Select *Show* and copy your new **OxfordKey**.
  ![](/images/psoxford/show-key.png)

  Now that we have the service side setup, we will use the **Oxford.ps1** script from [psoxford](https://github.com/zbrad/psoxford).  Easiest way to get this is to clone the repo, which will also get you our test images.

## PowerShell ##

### Setup ###

1. Launch a powershell session (I prefer to use the *Windows PowerShell ISE*.
1. Navigate to your clone
1. Import the script and set your key

```powershell
. .\Oxford.ps1
$key = 'put your oxford key here'
```

### Single File ###

We can now call the Oxford OCR and get results:

```powershell
$image = '.\images\ifwedid.jpg'
Get-Text -Image $image -OxfordKey $key
```

which altogether when run:

![](/images/psoxford/get-text-single.png)



### Multiple Files ###

That's fine for a single file, but what if we want all the files in a folder?  PowerShell to the rescue:

```powershell
$files = Get-ChildItem .\images | % { $_.FullName }
$files | Get-Text -OxfordKey $key
```

In this case PowerShell will call *Get-Text* cmdlet for each file in the folder.

![](/images/psoxford/get-text-multi.png)

## A Brief Look At The Script ##

The file *Oxford.ps1* defines 2 cmdlets:

- **Get-Text**
- **Invoke-Oxford**

The **Get-Text** cmdlet requires 2 mandatory parameters **Image** and **OxfordKey**.   The function is declared as:

```powershell
function Get-Text
{
[CmdletBinding()]
Param(
[Parameter(Mandatory=$true,ValueFromPipeline=$true)]
[string] $Image,
[Parameter(Mandatory=$true)]
[string] $OxfordKey
)
```

By allowing the **Image** parameter to be obtained from the pipeline, we enable the multi-file scenario.
The body of the function simply calls the **Invoke-Oxford** cmdlet, and then combines the text results for output.

The declaration of the **Invoke-Oxford** cmdlet is:

```powershell
function Invoke-Oxford
{
[CmdletBinding()]
Param(
[Parameter(Mandatory=$true)]
[string] $OxfordKey,
[string] $Api,
[string] $Lang = 'en',
[string] $Detect = $true,
[string] $InFile
)
```

## Summary ##

This was a brief afternoon hack to see if the Oxford OCR Api would be useful in my project.  Unfortunately for myself it was not, however
if this description and scripts helps others to determine that utility for themselves, it was worthwhile.


        


